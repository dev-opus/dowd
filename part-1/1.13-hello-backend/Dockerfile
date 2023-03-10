FROM golang:alpine3.17

WORKDIR /usr/src/app

COPY . .

RUN go build .

CMD [ "./server" ]

EXPOSE 8080