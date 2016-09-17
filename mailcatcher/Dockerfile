FROM ruby:2.3-alpine
MAINTAINER Boris Kraportov <boris.kraportov@gmail.com>
RUN apk add build-base sqlite-dev openssl-dev --no-cache
RUN gem install mailcatcher
# smtp port
EXPOSE 1025
# webserver port
EXPOSE 1080

find / -type f -iname \*.apk-new -delete && \
  rm -rf /var/cache/apk/* && \
  rm -rf /usr/lib/lib/ruby/gems/*/cache/* && \
  rm -rf ~/.gem

CMD ["mailcatcher", "-f", "--ip=0.0.0.0"]
