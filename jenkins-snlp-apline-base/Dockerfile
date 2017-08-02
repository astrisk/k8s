FROM jenkinsci/slave:2.62-alpine

MAINTAINER Qiusheng Zhang <fang_ruo@163.com>

USER root

RUN apk --no-cache add tzdata  && \
    ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && \
    echo "Asia/Shanghai" > /etc/timezone

USER jenkins

WORKDIR /home/jenkins

COPY jenkins-slave /usr/local/bin/jenkins-slave

ENTRYPOINT ["jenkins-slave"]
