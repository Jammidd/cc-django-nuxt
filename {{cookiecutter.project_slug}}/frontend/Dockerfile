FROM node:10

RUN mkdir -p /usr/src/nuxt-app
WORKDIR /usr/src/nuxt-app

RUN apt update && apt upgrade -y
RUN apt install git

COPY . /usr/src/nuxt-app/
RUN npm install

RUN npm run build
ENV HOST 0.0.0.0
EXPOSE 3000