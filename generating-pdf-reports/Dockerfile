FROM node:alpine

ENV NPM_CONFIG_PREFIX=/home/node/.npm-global \
    PATH=$PATH:/home/node/.npm-global/bin \
    NODE_PATH=/home/node/.npm-global/lib/node_modules/

RUN npm install -g puppeteer chart.js fs && \
    npm cache clean --force && \
    rm -rf /tmp/*