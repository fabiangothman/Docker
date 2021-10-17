FROM edyan/php:5.5

RUN apt update \
    && apt-get install git-core -y \
    && apt-get install nano -y \
    && apt-get install curl -y

RUN curl -sL https://deb.nodesource.com/setup_14.x | sudo -E bash - \
    && apt-get --force-yes install -y nodejs \
    && apt-get install -y build-essential
RUN npm install -g bower

ADD 20-xdebug.ini /etc/php5/fpm/conf.d/20-xdebug.ini

#
#
#FROM php:5.6-fpm-stretch
#
#RUN apt update \
#    && apt install mysql-client -y \
#    && apt install -y zlib1g-dev g++ git libicu-dev zip libzip-dev zip \
#    && docker-php-ext-install intl opcache pdo pdo_mysql mysqli bcmath \
#    && docker-php-ext-configure zip \
#    && docker-php-ext-install zip
#RUN curl -sL https://deb.nodesource.com/setup_14.x | bash - \
#    && apt-get install -y npm
#RUN npm install -g bower
#
#ENV PHP_OPCACHE_VALIDATE_TIMESTAMPS="0"
#ADD opcache.ini "$PHP_INI_DIR/conf.d/opcache.ini"
#ADD php.ini /usr/local/etc/php.ini
#
#RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
#
#RUN curl -sS https://get.symfony.com/cli/installer | bash
#RUN mv /root/.symfony/bin/symfony /usr/local/bin/symfony
##RUN git config --global user.email "you@example.com" \ 
##    && git config --global user.name "Your Name"
