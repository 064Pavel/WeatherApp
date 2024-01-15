# Используем официальный образ PHP 8.0 FPM
FROM php:8.3-fpm

# Устанавливаем Composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# Копируем кастомный php.ini
COPY ../configs/php.ini /usr/local/etc/php/conf.d/php.ini

# Устанавливаем пакеты, необходимые для установки Composer
RUN apt-get update && apt-get install -y \
    git \
    unzip

EXPOSE 9000

# Команда запуска PHP-FPM
CMD ["php-fpm"]