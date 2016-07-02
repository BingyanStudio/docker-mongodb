FROM alpine:edge

ENV MONGODB_VERSION 3.2.4

RUN echo "http://dl-4.alpinelinux.org/alpine/edge/testing" >> /etc/apk/repositories && \
    apk update && \
    apk add 'mongodb<3.2.5' && \
    mkdir -p /data/db && \
    chown -R mongodb /data/db && \
    rm -rf /var/cache/apk/*

VOLUME ["/data/db"]

EXPOSE 27017 28017

USER mongodb
CMD ["mongod"]
