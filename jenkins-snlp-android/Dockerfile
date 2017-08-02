FROM fangruo/jenkins-slave-ubuntu-base
MAINTAINER Qiusheng Zhang <fang_ruo@163.com>

ENV ANDROID_HOME /home/jenkins/android-sdk

USER root

RUN dpkg --add-architecture i386 && apt-get update && apt-get install -y libc6:i386 libncurses5:i386 libstdc++6:i386 lib32z1 && apt-get clean

USER jenkins
RUN mkdir /home/jenkins/android-sdk
VOLUME /home/jenkins/android-sdk
ENV PATH ${ANDROID_HOME}/tools:${ANDROID_HOME}/platform-tools:$PATH

RUN mkdir /home/jenkins/.gradle
VOLUME /home/jenkins/.gradle

ENV GRADLE_USER_HOME /home/jenkins/.gradle

WORKDIR /home/jenkins

