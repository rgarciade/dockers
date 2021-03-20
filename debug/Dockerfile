FROM php:7-apache
# Install XDebug
RUN pecl install -f xdebug \
&& echo "zend_extension=$(find /usr/local/lib/php/extensions/ -name xdebug.so)\nxdebug.mode=debug\nxdebug.start_with_request=yes" > /usr/local/etc/php/conf.d/xdebug.ini;
# Install net-tools which we'll need to set up host.docker.internal for Linux,
# you can do docker-php-ext-configure and docker-php-ext-install and install
# other dependencies as required here
RUN apt-get update \
    && apt-get install -y net-tools \
    && apt-get clean

CMD ["apache2-foreground"]