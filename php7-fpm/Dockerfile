FROM php:7.0-fpm

RUN apt-get update && apt-get install -y \
    git  \
    zip
#    procps \
#    vim

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
RUN composer --version

RUN rm /etc/localtime
RUN ln -s /usr/share/zoneinfo/Chile/Continental /etc/localtime
RUN "date"

RUN docker-php-ext-install pdo pdo_mysql
RUN docker-php-ext-install opcache
RUN pecl install apcu
RUN docker-php-ext-enable apcu
