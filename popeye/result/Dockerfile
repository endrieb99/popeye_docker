FROM node:12-alpine

MAINTAINER Endri Bida

RUN apk add --no-cache nodejs npm

WORKDIR /code

COPY . /code

RUN npm install

EXPOSE 80

ENTRYPOINT ["node"]

CMD ["Node.js"]