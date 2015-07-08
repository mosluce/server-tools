FROM ubuntu:14.04
MAINTAINER mosluce<mosluce@gmail.com>

RUN \
  apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 7F0CEB10 && \
  echo "deb http://repo.mongodb.org/apt/ubuntu "$(lsb_release -sc)"/mongodb-org/3.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.0.list && \
  apt-get update && \
  apt-get install -y mongodb-org && \
  mkdir -p /data/db

EXPOSE 27017
EXPOSE 28017

CMD ["mongod"]
