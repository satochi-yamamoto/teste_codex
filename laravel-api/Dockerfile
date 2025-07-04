FROM php:8.3-cli
WORKDIR /app
COPY . .
RUN apt-get update \
    && apt-get install -y libzip-dev unzip sqlite3 libsqlite3-dev libxml2-dev \
    && docker-php-ext-install pdo pdo_sqlite dom
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
RUN composer install --prefer-dist --no-interaction \
    && cp .env.example .env \
    && php artisan key:generate \
    && touch database/database.sqlite \
    && php artisan migrate --seed
CMD ["php", "artisan", "serve", "--host=0.0.0.0", "--port=8000"]
