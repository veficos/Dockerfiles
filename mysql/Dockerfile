FROM alpine:latest


WORKDIR /app
VOLUME /app

RUN sed -i 's/dl-cdn.alpinelinux.org/mirrors.ustc.edu.cn/g' /etc/apk/repositories && apk update
RUN  apk add --no-cache mysql && rm -f /var/cache/apk/*
COPY my.cnf /etc/mysql/my.cnf
COPY entrypoint.sh /entrypoint.sh

EXPOSE 3306
CMD ["/entrypoint.sh"]
