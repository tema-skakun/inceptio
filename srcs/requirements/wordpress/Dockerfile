FROM debian:buster

LABEL maintainer="tema_skakun@mail.ru"

RUN apt update && apt install -y php7.3 php-mysqli php-fpm curl sendmail

EXPOSE 9000

COPY ./conf/www.conf /etc/php/7.3/fpm/pool.d
COPY ./tools /var/www/
# static website
COPY conf/index.html /var/www/index.html

ENTRYPOINT bash /var/www/start.sh
