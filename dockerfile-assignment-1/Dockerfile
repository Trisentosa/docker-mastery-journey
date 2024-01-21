FROM node:6-alpine

EXPOSE 3000 

RUN apk add --no-cache tini

WORKDIR /user/src/app

COPY package.json package.json

RUN npm install \ 
    && npm cache clean --force

COPY . .

CMD ["tini","--","node","./bin/www"]