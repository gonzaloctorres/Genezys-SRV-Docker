ARG APACHE_VERSION
FROM httpd:$APACHE_VERSION-alpine

RUN apk update; \
    apk upgrade;

RUN apk add \
  bash \
  apache2 \
  php7-apache2 \
  curl \
  ca-certificates \
  openssl \
  git \
  php7 \
  php7-phar \
  php7-json \
  php7-iconv \
  php7-openssl \
  tzdata \
  openntpd \
  php7-ftp \
  php7-xdebug \
  php7-mcrypt \
  php7-mbstring \
  php7-soap \
  php7-gmp \
  php7-pdo_odbc \
  php7-dom \
  php7-pdo \
  php7-zip \
  php7-mysqli \
  php7-bcmath \
  php7-gd \
  php7-odbc \
  php7-pdo_mysql \
  php7-gettext \
  php7-xmlreader \
  php7-xmlwriter \
  php7-tokenizer \
  php7-xmlrpc \
  php7-bz2 \
  php7-pdo_dblib \
  php7-curl \
  php7-ctype \
  php7-session \
  php7-exif \
  nodejs;

RUN sed -i "s/#LoadModule\ rewrite_module/LoadModule\ rewrite_module/" /usr/local/apache2/conf/httpd.conf;

RUN mkdir -p /var/www/vhosts

COPY ambientes.conf /usr/local/apache2/conf/ambientes.conf
RUN echo "Include /usr/local/apache2/conf/ambientes.conf" \
    >> /usr/local/apache2/conf/httpd.conf