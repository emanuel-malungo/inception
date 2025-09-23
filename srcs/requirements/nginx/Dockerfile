FROM debian:bullseye

RUN apt update && apt install -y --no-install-recommends \
    nginx \
    openssl \
    && rm -rf /var/lib/apt/lists/* \
    && mkdir -p /etc/ssl/mycerts 

COPY ./srcs/requirements/nginx/nginx.conf /etc/nginx/nginx.conf