# Pull in the from the official nginx image.
FROM nginx

EXPOSE 80

# Delete the default welcome to nginx page.
RUN rm /usr/share/nginx/html/*

# Copy over the custom default configs - coming from nginx default.config
COPY configs/default.conf /etc/nginx/conf.d/default.conf

# Start nginx in the foreground to play nicely with Docker.
CMD ["nginx", "-g", "daemon off;"]
