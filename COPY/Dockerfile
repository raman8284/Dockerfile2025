# Use the latest Ubuntu base image
FROM ubuntu:latest

# Set the maintainer label
#LABEL maintainer="yourname@example.com"

# Update package lists and install Nginx
RUN apt-get update && apt-get install -y nginx && rm -rf /var/lib/apt/lists/*

# Copy the static site files to Nginx's default HTML folder
COPY qi/ /var/www/html/

# Expose Nginx's default port
#EXPOSE 80

# Start Nginx in the foreground
CMD ["nginx", "-g", "daemon off;"]
