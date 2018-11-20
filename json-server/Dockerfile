FROM alpine
MAINTAINER Chris Quan

WORKDIR /app

RUN set -xe \
    && apk add --no-cache nodejs nodejs-npm \
    && npm install -g json-server \
    && rm -rf /tmp/npm* /var/cache/apk/*

ENTRYPOINT ["json-server"]