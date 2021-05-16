FROM node:14.15.3-alpine3.11

RUN apk update && \
    apk upgrade && \
    npm install --ignore-scripts -g oval

COPY linter.sh /bin

ENTRYPOINT ["linter.sh"]
