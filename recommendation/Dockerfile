FROM golang:1.20-alpine

WORKDIR /recommendation

COPY ./recommendation /recommendation

RUN go build -o app

EXPOSE 8080

CMD ["./app"]