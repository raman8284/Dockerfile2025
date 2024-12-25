# Use the official Ubuntu image
FROM ubuntu:20.04

# Set environment variable to avoid interactive prompts during package installation
ENV DEBIAN_FRONTEND=noninteractive

# Install Nginx and any necessary utilities
RUN apt update && apt install -y \
    nginx \
    && apt clean \
    && rm -rf /var/lib/apt/lists/*

# Remove the default Nginx welcome page
RUN rm -rf /usr/share/nginx/html/index.html

# Copy your static website files into the container
# Make sure you have a local folder named 'mywebsite' containing your static files (index.html, CSS, JS)
COPY mywebsite/ /usr/share/nginx/html/

# Change ownership of the files so Nginx can access them
RUN chown -R www-data:www-data /usr/share/nginx/html \
    && chmod -R 755 /usr/share/nginx/html

# Expose port 80 for HTTP traffic
EXPOSE 80

# Start Nginx in the foreground
CMD ["nginx", "-g", "daemon off;"]
