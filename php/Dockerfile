FROM php:7.4-apache
RUN a2enmod rewrite
RUN apt-get update && apt-get install -y \
    gnupg \
    libzip-dev \
    unzip \
    zlib1g-dev \
    libonig-dev \
    git \
    vim \
    && docker-php-ext-install \
    opcache \
    zip \
    pdo_mysql \
    mysqli \
    mbstring

WORKDIR /var/www/src

COPY --from=composer:2.2.5 /usr/bin/composer /usr/bin/composer