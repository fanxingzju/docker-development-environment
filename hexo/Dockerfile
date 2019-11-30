FROM ubuntu:16.04
MAINTAINER fanxingzju "fanxingzju@gmail.com"

USER root
ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update && \
    apt-get install -y wget sudo git git-core firefox vim xz-utils && \
	apt-get install -y language-pack-zh-hans zh-autoconvert zhcon && \
    apt-get clean && apt-get purge && apt-get autoremove && rm -rf /var/lib/apt/lists/* && \
	echo "set fileencodings=utf-8,gb2312,gbk,gb18030" >> /etc/vim/vimrc && \
	echo "set termencoding=utf-8" >> /etc/vim/vimrc && \
	echo "set encoding=prc" >> /etc/vim/vimrc

RUN mkdir -p /tmp/nodejs && \
    wget https://nodejs.org/dist/v10.9.0/node-v10.9.0-linux-x64.tar.xz -O /tmp/nodejs.tar.xz --no-check-certificate && \
    tar -xf /tmp/nodejs.tar.xz -C /tmp/nodejs --strip-components 1 && \
    cp -r /tmp/nodejs/bin/* /usr/local/bin/ && \
    cp -r /tmp/nodejs/include/* /usr/local/include/ && \
    cp -r /tmp/nodejs/lib/* /usr/local/lib/ && \
    rm -rf /tmp/* 

RUN npm install -g hexo-cli --registry=https://registry.npm.taobao.org

WORKDIR /home
CMD /bin/bash

