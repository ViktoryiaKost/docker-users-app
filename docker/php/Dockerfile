FROM php:8.3-fpm

RUN docker-php-ext-install mysqli

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/bin --filename=composer && chmod +x /usr/bin/composer

ENV COMPOSER_ALLOW_SUPERUSER=1

RUN pecl install xdebug \
    && docker-php-ext-enable xdebug

COPY conf.d/* /usr/local/etc/php/conf.d


