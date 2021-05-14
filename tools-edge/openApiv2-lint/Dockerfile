FROM node:lts-alpine

RUN apk update && \
    apk upgrade && \
    npm install --ignore-scripts -g oval

COPY linter.sh /bin

ENTRYPOINT ["linter.sh"]
