FROM node:0.12.6
MAINTAINER mosluce<mosluce@gmail.com>

RUN \
  npm install pm2 -g && \
  npm install express-generator -g && \
  mkdir /app

RUN \
  echo '#!/bin/sh' >> start && \
  echo 'cd /app' >> start && \
  echo 'npm install' >> start && \
  echo 'pm2 start -i max bin/www' >> start && \
  echo 'bash' >> start && \
  chmod +x start

WORKDIR /

VOLUME [/app]

EXPOSE 8080

ENV NODE_ENV production
ENV PORT 8080

CMD ["./start"]


