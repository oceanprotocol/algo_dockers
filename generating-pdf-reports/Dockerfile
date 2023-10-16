FROM node:alpine

RUN apk update && apk add chromium

ENV NPM_CONFIG_PREFIX=/home/node/.npm-global \
    PATH=$PATH:/home/node/.npm-global/bin \
    PUPPETEER_EXECUTABLE_PATH=/usr/bin/chromium-browser \
    NODE_PATH=/home/node/.npm-global/lib/node_modules/

RUN npm install -g puppeteer chart.js fs && \
    npm cache clean --force && \
    rm -rf /tmp/*