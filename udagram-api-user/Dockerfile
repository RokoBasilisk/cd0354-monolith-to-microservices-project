FROM node:16.20.2
## Create app directory
WORKDIR /usr/src/app
## Install app dependencies
## A wildcard is used to ensure both package.json AND package-lock.json are copied where available (npm@5+)
COPY package*.json ./
run npm ci -f
## Bundle app source
COPY . .
EXPOSE 8080
CMD [ "npm", "run", "prod" ]