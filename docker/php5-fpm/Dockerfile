# Pull docker base image
FROM php:5.6-fpm

# Add php configs file to the image
COPY ./docker/php5-fpm/configs/php.ini /usr/local/etc/php/
COPY ./docker/php5-fpm/configs/php-fpm.conf /usr/local/etc/php/

# Install php extentions and dependencies
RUN apt-get update && \
    apt-get install -y && \
    apt-get install -y libfreetype6-dev && \
    apt-get install -y libjpeg62-turbo-dev && \
    apt-get install -y libmcrypt-dev && \
    apt-get install -y libpng12-dev && \
    apt-get install -y && \
    apt-get install -y && \
    apt-get install -y vim && \
    apt-get install -y wget && \
    apt-get install -y unzip && \
    apt-get install -y git && \
    docker-php-ext-install -j$(nproc) iconv intl xml soap mcrypt opcache pdo pdo_mysql mysqli mbstring && \
    docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ && \
    docker-php-ext-install -j$(nproc) gd
