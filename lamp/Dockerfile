FROM alpine:3.13

LABEL maintainer="Ernesto Liberio <ernesto.liberio@gmail.com>" \
      description="Contenedor para Laravel"

ENV TZ=America/Guayaquil
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

RUN apk update && apk upgrade
RUN apk add apache2 \
    apache2-utils \
    curl wget \
    tzdata \
    php7-apache2 \
    php7-cli \
    php7-phar \
    php7-zlib \
    php7-zip \
    php7-bz2 \
    php7-ctype \
    php7-curl \
    php7-pdo_mysql \
    php7-mysqli \
    php7-json \
    php7-mcrypt \
    php7-xml \
    php7-dom \
    php7-iconv \
    php7-xdebug \
    php7-session \
    php7-intl \
    php7-gd \
    php7-ldap \
    php7-soap \
    php7-ftp \
    php7-mbstring \
    php7-apcu \
    php7-opcache \
    php7-tokenizer \
    php7-simplexml \
    php7-fileinfo \
    php7-redis \
    php7-mongodb \
    freetds-dev \
    php7-fileinfo \
    php7-pdo_dblib \
    unixodbc


RUN curl -sS https://getcomposer.org/installer | \
    php -- --install-dir=/usr/bin --filename=composer


RUN mkdir /var/www/html/

EXPOSE 80

# start apache
CMD httpd
