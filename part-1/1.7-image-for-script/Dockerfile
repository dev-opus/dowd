FROM ubuntu:20.04

WORKDIR /~/src/app

COPY script.sh .

RUN apt-get update && \
    apt-get -y install curl

CMD [ "./script.sh" ]