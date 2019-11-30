FROM python:3.7.4-buster
MAINTAINER fanxingzju "fanxingzju@gmail.com"

USER root
ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update && \
    apt-get install -y wget git vim openjdk-11-jre && \
    apt-get clean && apt-get purge && apt-get autoremove && rm -rf /var/lib/apt/lists/*

RUN mkdir -p /pycharm && \
    wget https://download.jetbrains.com/python/pycharm-community-2018.3.7.tar.gz -O /tmp/pycharm.tar.gz --no-check-certificate && \
    tar -xzvf /tmp/pycharm.tar.gz -C /pycharm --strip-components 1 && \
    rm -rf /tmp/*

WORKDIR /pycharm
CMD /bin/bash
