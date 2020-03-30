FROM circleci/php:7.4.4-node-browsers

RUN set -ex \
    && sudo docker-php-ext-install bcmath

USER root

RUN set -ex \
    && sudo pecl install redis \
    && sudo echo "extension=redis.so" > /usr/local/etc/php/conf.d/redis.ini

USER circleci