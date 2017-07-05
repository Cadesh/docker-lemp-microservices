# Pull docker base image
FROM php:5.6-fpm

# Add php configs file to the image
COPY ./configs/php.ini /usr/local/etc/php/

# Install php extentions and dependencies
RUN apt-get update && apt-get install -y \
            libfreetype6-dev \
            libjpeg62-turbo-dev \
            libmcrypt-dev \
            libpng12-dev \
            libicu-dev \
            libxml2-dev \
            vim \
            wget \
            unzip \
            git \
            && docker-php-ext-install -j$(nproc) iconv intl xml soap mcrypt opcache pdo pdo_mysql mysqli mbstring \
            && docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
            && docker-php-ext-install -j$(nproc) gd
