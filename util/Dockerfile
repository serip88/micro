FROM felixnilam/php5.4-apache-ext

WORKDIR /app

COPY composer.json composer.phar .

RUN phar install -g composer/composer

COPY . .

RUN composer install

EXPOSE 81

CMD ["php", "-S", "0.0.0.0:81"]
