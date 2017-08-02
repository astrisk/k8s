FROM jenkins:2.46.3-alpine

MAINTAINER Qiusheng Zhang <fang_ruo@163.com>

USER root

RUN apk --no-cache add tzdata  && \
    ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && \
    echo "Asia/Shanghai" > /etc/timezone

USER jenkins

