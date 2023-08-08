FROM php:7.2-apache

# Install dependencies
RUN apt-get update && apt-get install -y \
    libpng-dev \
    zlib1g-dev \
    libxml2-dev \
    libzip-dev \
    libonig-dev \
    zip \
    curl

# Install extensions
RUN docker-php-ext-install pdo_mysql mbstring zip exif pcntl bcmath gd

# Download specific version of Composer
RUN curl -o /usr/local/bin/composer https://getcomposer.org/download/2.0.0/composer.phar

# Make Composer executable
RUN chmod +x /usr/local/bin/composer

# Set working directory
WORKDIR /var/www

# Change ownership of our applications
RUN chown -R www-data:www-data /var/www

# Configure Apache
RUN sed -i 's!/var/www/html!/var/www/public!g' /etc/apache2/sites-available/000-default.conf
RUN a2enmod rewrite

# Expose port 80 and start apache server
EXPOSE 80
CMD ["apache2-foreground"]