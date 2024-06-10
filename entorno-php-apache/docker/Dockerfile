FROM ubuntu:22.04
ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update && apt-get install -y wget net-tools vim apache2 curl git unzip
RUN apt-get install software-properties-common -y
RUN add-apt-repository ppa:ondrej/php
RUN apt-get install -y apt-utils php8.2 php-xml php-mbstring php-mysql libapache2-mod-php
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
ENTRYPOINT service apache2 start && tail -f /var/log/apache2/error.log