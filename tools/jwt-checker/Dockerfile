FROM golang:1.14.2-buster AS build

RUN apt update && apt upgrade -y

COPY jwtvalidator/ /jwtvalidator

WORKDIR /jwtvalidator

RUN go test ./... && \
    go build -o jwt-checker

FROM alpine:3.17

WORKDIR /root/

COPY --from=build /jwtvalidator/jwt-checker .

ENTRYPOINT ["./jwt-checker"]
