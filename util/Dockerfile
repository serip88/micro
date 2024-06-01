# version name:  php8.2.v4
# Use the official PHP image with Apache and PHP 8.2
FROM php:8.2-apache

# Install additional PHP extensions if needed
RUN docker-php-ext-install mysqli

# Install Git
RUN apt-get update && apt-get install -y git vim && rm -rf /var/lib/apt/lists/*

# Copy application files to the web server's root directory
COPY . /var/www/html/

# Set permissions for the web server
RUN chown -R www-data:www-data /var/www/html \
    && chmod -R 755 /var/www/html

# Expose port 80 to be accessible outside the container
EXPOSE 80

# Start Apache in the foreground
CMD ["apache2-foreground"]
