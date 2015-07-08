FROM node:0.12.6
MAINTAINER mosluce<mosluce@gmail.com>

RUN \
  npm install pm2 -g && \
  npm install express-generator -g && \
  mkdir /app

WORKDIR /app

RUN \
  express . && \
  npm install

VOLUME [/app]

EXPOSE 8080

ENV NODE_ENV production
ENV PORT 8080

CMD ["npm install && pm2 start -i max bin/www"]


