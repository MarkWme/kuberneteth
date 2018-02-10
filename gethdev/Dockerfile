FROM node:9.5.0-alpine

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

RUN apk add -t .gyp --no-cache git python g++ make \
    && npm install -g truffle@3.2.x \
    && apk del .gyp && npm build

# ENTRYPOINT ["truffle"]
# CMD ["sh", "-c", "tail -f /dev/null"]