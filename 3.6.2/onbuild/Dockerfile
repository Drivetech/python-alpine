FROM drivetech/python-alpine:3.6.2

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

ONBUILD COPY requirements.txt /usr/src/app/
ONBUILD RUN pip install --no-cache-dir -r requirements.txt

ONBUILD COPY . /usr/src/app

ONBUILD RUN npm i && npm run build && npm cache clean --force && \
  apk del .npm-build-deps && \
  rm -rf ~/.node-gyp /tmp/* ~/.cache/bower ~/.npm bower_components node_modules
