FROM node:14.17.3-alpine3.11

RUN apk update && \
    apk upgrade && \
    npm install -g speccy

COPY linter.sh /bin

ENTRYPOINT ["linter.sh"]
