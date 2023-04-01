FROM golang:alpine3.17

WORKDIR /usr/src/app

COPY . .

ENV REQUEST_ORIGIN=http://localhost:5000

RUN go build .

RUN adduser -D -g '' appuser

RUN chown appuser .

USER appuser

CMD [ "./server" ]

EXPOSE 8080