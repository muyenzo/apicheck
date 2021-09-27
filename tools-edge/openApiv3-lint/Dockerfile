FROM node:fermium-alpine

RUN apk update && \
    apk upgrade && \
    npm install -g speccy

COPY linter.sh /bin

ENTRYPOINT ["linter.sh"]
