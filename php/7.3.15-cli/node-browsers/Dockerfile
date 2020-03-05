FROM circleci/php:7.3.15-node-browsers

RUN set -ex; \
    sudo apt update && \
    sudo apt install -y libgmp-dev && \
    sudo rm -rf /var/lib/api/lists*

RUN set -ex; \
    sudo docker-php-ext-install bcmath gmp