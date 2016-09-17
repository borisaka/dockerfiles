FROM ruby:2.3-alpine
MAINTAINER Boris Kraportov <boris.kraportov@gmail.com>
RUN apk add --no-cache --virtual build-dependencies \
    build-base \
    openssl-dev \
    sqlite-dev && \
    gem install mailcatcher && \
    apk del build-dependencies && \
    rm -rf  $GEM_HOME/cache/* 

# smtp port
EXPOSE 1025
# webserver port
EXPOSE 1080

CMD ["mailcatcher", "-f", "--ip=0.0.0.0"]
