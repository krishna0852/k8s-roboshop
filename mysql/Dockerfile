ARG VERSION=5.7

FROM mysql:${VERSION}

VOLUME /data

ENV MYSQL_ALLOW_EMPTY_PASSWORD=yes \
    MYSQL_DATABASE=cities

COPY config.sh /root/

RUN chmod +x /root/config.sh

RUN /root/config.sh

COPY scripts/* /docker-entrypoint-initdb.d/
