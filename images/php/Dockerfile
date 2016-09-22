FROM php:5.6-fpm
RUN apt-get update && apt-get install -y libmcrypt-dev 

# lumen packages
RUN apt-get install -y php5-memcached 
RUN docker-php-ext-install mcrypt mbstring tokenizer mysqli pdo_mysql

RUN apt-get install zlib1g-dev

# Install the php memcached extension
RUN pecl install memcached && \
    docker-php-ext-enable memcached \