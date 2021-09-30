FROM php:8.0-fpm-alpine

RUN apk add --no-cache openssl bash mysql-client nodejs npm

RUN docker-php-ext-install pdo pdo_mysql bcmath

WORKDIR /var/www

RUN rm -rf /var/www/html
RUN ln -s projeto html

RUN curl -sS http://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

EXPOSE 9001

ENTRYPOINT ["php-fpm"]

