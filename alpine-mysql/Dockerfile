FROM alpine
#MAINTAINER WangXian <xian366@126.com>
LABEL maintainer "lorenwe <lorenwe@kaolanet.com>" architecture="AMD64/x86_64"  mysqlversion="5.6"

WORKDIR /app
VOLUME /app
COPY startup.sh /startup.sh

RUN apk add --update mysql mysql-client && rm -f /var/cache/apk/*
COPY my.cnf /etc/mysql/my.cnf

RUN chmod 644 /etc/mysql/my.cnf

EXPOSE 3306
CMD ["/startup.sh"]
