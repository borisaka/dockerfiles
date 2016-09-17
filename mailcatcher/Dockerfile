FROM ruby:2.3-alpine
MAINTAINER Boris Kraportov <boris.kraportov@gmail.com>
RUN apk add build-base sqlite-dev openssl-dev --no-cache
RUN gem install mailcatcher
# smtp port
EXPOSE 1025
# webserver port
EXPOSE 1080

CMD ["mailcatcher", "-f", "--ip=0.0.0.0"]
