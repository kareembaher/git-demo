# Use the official Ubuntu base image
FROM ubuntu:latest

# Update the package list and install Apache2
RUN apt-get update && \
    apt-get install -y apache2 && \
    apt-get clean

# Copy the Apache configuration and web content into the image
COPY html/index.html /var/www/html/index.html

# Expose port 80 to allow external access to the web server
EXPOSE 80

# Start Apache2 in the foreground
CMD ["apachectl", "-D", "FOREGROUND"]
