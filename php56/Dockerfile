FROM bitrixdock/php56-fpm:latest

ADD ./php.ini /etc/php5/fpm/conf.d/90-php.ini
ADD ./php.ini /etc/php5/cli/conf.d/90-php.ini

RUN sed -i 's/:9000/:9100/' /etc/php5/fpm/pool.d/www.conf

RUN usermod -u 1000 www-data

WORKDIR "/var/www/bitrix"

EXPOSE 9100