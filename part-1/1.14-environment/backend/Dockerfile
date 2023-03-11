FROM golang:alpine3.17

WORKDIR /usr/src/app

COPY . .

ENV REQUEST_ORIGIN=http://localhost:5000

RUN go build .

CMD [ "./server" ]

EXPOSE 8080