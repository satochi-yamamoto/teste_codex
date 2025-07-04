FROM php:8.3-cli
WORKDIR /app
COPY . .
RUN apt-get update \
    && apt-get install -y libzip-dev unzip \
    && docker-php-ext-install pdo pdo_sqlite
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
RUN composer install --no-dev --prefer-dist --no-interaction
CMD ["php", "artisan", "serve", "--host=0.0.0.0", "--port=8000"]
