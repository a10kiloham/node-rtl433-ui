FROM node:16-alpine

VOLUME ["/raspiscan/frontend/node_modules"]
RUN apk add --update python3 make g++\
   && rm -rf /var/cache/apk/*
RUN npm config set legacy-peer-deps true

WORKDIR /raspiscan/frontend
COPY frontend/package.json .
RUN npm install
COPY frontend .

WORKDIR /raspiscan
COPY .env.example .env
