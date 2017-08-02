FROM jenkinsci/slave:2.62

MAINTAINER Qiusheng Zhang <fang_ruo@163.com>

USER root

RUN echo "Asia/Shanghai" > /etc/timezone && \
    dpkg-reconfigure -f noninteractive tzdata
USER jenkins

WORKDIR /home/jenkins

COPY jenkins-slave /usr/local/bin/jenkins-slave

ENTRYPOINT ["jenkins-slave"]
