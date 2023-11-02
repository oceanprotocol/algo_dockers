FROM node:alpine

ENV NPM_CONFIG_PREFIX=/home/node/.npm-global \
    PATH=$PATH:/home/node/.npm-global/bin \
    NODE_PATH=/home/node/.npm-global/lib/node_modules/ \
    PYTHONUNBUFFERED=1

RUN apk update && \
    apk add ffmpeg && \
    apk add --update --no-cache python3 && \
    apk add pkgconfig && \
    apk add g++ && \
    apk add jpeg-dev && \
    apk add cairo-dev && \
    apk add giflib-dev && \
    apk add pango-dev && \
    apk add libtool && \
    apk add autoconf && \
    apk add automake && \
    apk add libpng && \
    apk add libpng-dev && \
    apk add build-base && \
    apk --no-cache add ca-certificates wget  && \
        wget -q -O /etc/apk/keys/sgerrand.rsa.pub https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub && \
        wget https://github.com/sgerrand/alpine-pkg-glibc/releases/download/2.29-r0/glibc-2.29-r0.apk && \
    apk add --force-overwrite glibc-2.29-r0.apk && \
    ln -sf python3 /usr/bin/python && \
    python3 -m ensurepip && \
    pip3 install --no-cache --upgrade pip setuptools
   

WORKDIR /usr/app
COPY . /usr/app

RUN npm install && \
    npm cache clean --force 