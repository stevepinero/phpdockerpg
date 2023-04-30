FROM php:8.2-fpm-alpine:latest
WORKDIR "/application"

# Fix debconf warnings upon build
ARG DEBIAN_FRONTEND=noninteractive

# Install selected extensions and other stuff
RUN apt-get update; \
    apt-get -y --no-install-recommends install \
        php8.2-bcmath \ 
        php8.2-bz2 \ 
        php8.2-gd \ 
        php8.2-mysql \ 
        php8.2-uuid \ 
        php8.2-xdebug \
        php8.2-xmlrpc \
        php8.2-xsl \ 
        php8.2-yaml; \
    apt-get clean; \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*

#RUN apt-get update \
#    && apt-get -y --no-install-recommends install  php8.2-pgsql php8.2-xdebug php8.2-bcmath php8.2-bz2 php8.2-gd php8.2-xmlrpc \
#    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*