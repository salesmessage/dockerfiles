FROM circleci/php:7.3.16-cli-buster

RUN set -ex \
    && sudo apt update \
    && sudo apt install -y libgmp-dev \
    && sudo rm -rf /var/lib/api/lists*

RUN set -ex \
    && sudo docker-php-ext-install bcmath gmp

USER root

RUN set -ex \
    && sudo pecl install redis \
    && sudo echo "extension=redis.so" > /usr/local/etc/php/conf.d/redis.ini

USER circleci
