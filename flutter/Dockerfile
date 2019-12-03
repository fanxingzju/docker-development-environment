FROM ubuntu:16.04
MAINTAINER fanxingzju "fanxingzju@gmail.com"

USER root
ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update && \
    apt-get install -y wget vim openjdk-9-jre firefox git libpulse-dev curl && \
    apt-get install -y xz-utils && \
    apt-get clean && apt-get purge && apt-get autoremove && rm -rf /var/lib/apt/lists/*

RUN mkdir -p /android-studio && \
    wget https://dl.google.com/dl/android/studio/ide-zips/3.5.2.0/android-studio-ide-191.5977832-linux.tar.gz -O /tmp/android-studio.tar.gz --no-check-certificate && \
    tar -xzvf /tmp/android-studio.tar.gz -C /android-studio --strip-components 1 && \
    rm -rf /tmp/*

RUN mkdir -p /flutter && \
    wget https://storage.googleapis.com/flutter_infra/releases/stable/linux/flutter_linux_v1.9.1+hotfix.6-stable.tar.xz -O /tmp/flutter.tar.xz --no-check-certificate && \
    tar -xf /tmp/flutter.tar.xz -C /flutter --strip-components 1 && \
    rm -rf /tmp/*

WORKDIR /flutter
CMD /bin/bash

