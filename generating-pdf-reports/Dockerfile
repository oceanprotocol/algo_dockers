FROM node:latest

ENV NPM_CONFIG_PREFIX=/home/node/.npm-global
ENV PATH=$PATH:/home/node/.npm-global/bin
RUN npm install -g puppeteer \
 chart.js \
 fs
ENV NODE_PATH=/home/node/.npm-global/lib/node_modules/