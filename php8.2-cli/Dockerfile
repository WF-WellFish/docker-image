FROM php:8.2-cli

# Install dependencies
RUN apt-get update && apt-get install -y \
    libpng-dev \
    libjpeg-dev \
    libfreetype6-dev \
    libonig-dev \
    libxml2-dev \
    libzip-dev \
    unzip

# Install extensions
RUN docker-php-ext-install pdo pdo_mysql gd zip bcmath

# Configure gd
RUN docker-php-ext-configure gd --enable-gd --with-jpeg

# Install gd
RUN docker-php-ext-install gd
