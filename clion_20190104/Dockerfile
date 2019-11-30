FROM ubuntu:16.04
MAINTAINER fanxingzju "fanxingzju@gmail.com"

USER root
ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update && \
    apt-get install -y clang cmake g++ gcc wget gdb sudo git firefox vim && \
    apt-get clean && apt-get purge && apt-get autoremove && rm -rf /var/lib/apt/lists/*

RUN mkdir -p /clion && \
    wget https://download.jetbrains.com/cpp/CLion-2019.1.4.tar.gz -O /tmp/clion.tar.gz --no-check-certificate && \
    tar -xzvf /tmp/clion.tar.gz -C /clion --strip-components 1 && \
    chmod +x /clion/bin/clion.sh && \
    rm -rf /tmp/*

WORKDIR /clion
CMD /bin/bash

