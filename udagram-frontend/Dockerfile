### Build
FROM node:16.20.2 AS build
## Create app directory
WORKDIR /usr/src/app
## Install app dependencies
## A wildcard is used to ensure both package.json AND package-lock.json are copied
COPY package*.json ./
CMD [ "npm", "ci"]
## Bundle app source
COPY . .
CMD [ "ionic", "build"]
### Run 
FROM nginx:alpine
#COPY www /usr/share/nginx/html
COPY --from=build /usr/src/app/www /usr/share/nginx/html