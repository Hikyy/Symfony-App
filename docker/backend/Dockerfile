FROM php:8.2-fpm

RUN apt-get update && \
    apt-get install -y \
        libbz2-dev \
        libcurl4-openssl-dev \
        libonig-dev \
        libxml2-dev \
        libzip-dev \
        unzip \
        curl

RUN docker-php-ext-install \
    bz2 \
    curl \
    mbstring \
    intl \
    pdo \
    pdo_mysql \
    xml


WORKDIR /var/www/html/symfony_app

COPY ../../ .

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

RUN curl -1sLf 'https://dl.cloudsmith.io/public/symfony/stable/setup.deb.sh' | bash && \
        apt-get install -y symfony-cli

RUN usermod -u 1000 www-data

CMD php-fpm
