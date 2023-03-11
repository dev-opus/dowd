FROM node:lts-bullseye-slim

WORKDIR /usr/src/app

COPY package*.json .

RUN npm ci

# added these lines (11 and  13) to fix bug related to postcss (see this reddit commment: https://www.reddit.com/r/learnreactjs/comments/qs7urz/comment/hpsrk7h/?utm_source=share&utm_medium=web2x&context=3)

RUN npm i -D postcss@latest

ENV NODE_OPTIONS=--openssl-legacy-provider
ENV REACT_APP_BACKEND_URL=http://localhost:8080

COPY . .

RUN npm run build

EXPOSE 5000

CMD [ "npx", "serve", "-s", "-l", "5000", "build" ]

