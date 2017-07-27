FROM drivetech/python-alpine:2.7.13

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

ONBUILD COPY requirements.txt /usr/src/app/
ONBUILD RUN pip install --no-cache-dir -r requirements.txt

ONBUILD COPY . /usr/src/app

ONBUILD RUN apk add --no-cache --virtual .npm-build-deps nodejs-current-npm git && \
  npm i && npm run build:production && npm cache clean --force && \
  apk del .npm-build-deps && \
  rm -rf ~/.node-gyp /tmp/* ~/.cache/bower ~/.npm bower_components node_modules

