FROM node:8.4.0-alpine
MAINTAINER Dragos Bulugean

RUN apk update && apk add --no-cache bash git make gcc g++ python py-pip py-setuptools ca-certificates openssl curl zip
RUN pip --no-cache-dir install awscli 
RUN update-ca-certificates

ENV DOCKERIZE_VERSION v0.5.0
RUN wget https://github.com/jwilder/dockerize/releases/download/$DOCKERIZE_VERSION/dockerize-alpine-linux-amd64-$DOCKERIZE_VERSION.tar.gz \
    && tar -C /usr/local/bin -xzvf dockerize-alpine-linux-amd64-$DOCKERIZE_VERSION.tar.gz \
    && rm dockerize-alpine-linux-amd64-$DOCKERIZE_VERSION.tar.gz

ENV DOCKER_VERSION=17.03.0-ce
RUN wget https://get.docker.com/builds/Linux/x86_64/docker-$DOCKER_VERSION.tgz \
    && tar -C /usr/local/bin -xzvf docker-$DOCKER_VERSION.tgz --strip-components=1 \
    && rm docker-$DOCKER_VERSION.tgz

   