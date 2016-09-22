FROM php:5.6-fpm
RUN apt-get update && apt-get install -y libmcrypt-dev 

# lumen packages
RUN apt-get install -y php5-memcached zlib1g-dev
RUN docker-php-ext-install mcrypt mbstring tokenizer mysqli pdo_mysql

# Install the php memcached extension
RUN pecl install memcached && \
    docker-php-ext-enable memcached \