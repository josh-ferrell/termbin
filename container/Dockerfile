FROM nginx:stable

ADD fiche /usr/bin/fiche
ADD default.conf /etc/nginx/conf.d/
ADD nginx.conf /etc/nginx/

RUN apt update -y \
	&& apt upgrade -y \
	&& rm -rf /var/cache/* 

ADD 30-fiche.sh /docker-entrypoint.d/
