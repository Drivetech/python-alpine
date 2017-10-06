FROM python:2.7.14-alpine3.6

LABEL maintainer "Leonardo Gatica <lgatica@protonmail.com>"

ENV TERM xterm

RUN apk add --no-cache --virtual build-dependencies postgresql-dev make gcc \
  g++ ca-certificates zlib-dev jpeg-dev tiff-dev freetype-dev lcms2-dev \
  libwebp-dev tcl-dev tk-dev libxml2-dev libxslt-dev libffi-dev && \
  apk add --no-cache git && apk add --no-cache \
  --repository http://dl-4.alpinelinux.org/alpine/edge/community/ \
  --virtual .npm-build-deps nodejs-current-npm
