FROM php:8.2-cli

# Instala Composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# Instala Xdebug
RUN pecl install xdebug \
    && docker-php-ext-enable xdebug

# Configura Xdebug
RUN echo "xdebug.mode=debug" >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini \
    && echo "xdebug.start_with_request=yes" >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini \
    && echo "xdebug.client_host=host.docker.internal" >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini

# Configura el directorio de trabajo
WORKDIR /var/www/html

# Expone el puerto 9000 para la depuración
EXPOSE 9000

# Ejecuta el servidor PHP
CMD ["php", "-S", "0.0.0.0:9000"]

