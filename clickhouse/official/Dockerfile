FROM yandex/clickhouse-server:19.8

ENV LANG ru_RU.UTF-8

MAINTAINER mail@flexberry.ru

RUN \
    apt-get update; \
    apt-get install -y less vim psmisc telnet postgresql-client unixodbc odbcinst odbc-postgresql xsltproc libxml2-utils

COPY /docker-entrypoint-initdb.d /docker-entrypoint-initdb.d

# ENTRYPOINT "/entrypoint.sh gosu clickhouse:clickhouse /usr/bin/clickhouse-server --config-file=/etc/clickhouse-server/config.xml"
