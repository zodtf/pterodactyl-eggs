FROM node:16-alpine

LABEL author="zudsniper" maintainer="support@zod.tf"

RUN apk add --no-cache --update curl ca-certificates openssl git tar bash sqlite fontconfig \
    && adduser --disabled-password --home /home/container container \
    && npm install -g @types/node \
    && npm install -g typescript

USER container
ENV  USER=container HOME=/home/container

WORKDIR /home/container

COPY ./entrypoint.sh /entrypoint.sh

CMD ["/bin/bash", "/entrypoint.sh"]
