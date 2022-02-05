FROM php:7.2-apache
MAINTAINER 'Matheus Rosmaninho <rosmaninho@ufv.br>'

RUN apt -y update
RUN docker-php-ext-install mysqli && docker-php-ext-enable mysqli
RUN apt install -y wget git vim htop unzip

# Executa permissões no diretório

RUN find . -type d -exec chmod 0755 {} \;
RUN find . -type f -exec chmod 0644 {} \;

# Adiciona permissão pro seu usuário na pasta www
CMD usermod -u `stat -c %u /var/www/html` www-data && groupmod -g `stat -c %g /var/www/html` www-data
CMD chsh -s /bin/bash www-data

# Executa o apache
CMD apachectl -D FOREGROUND