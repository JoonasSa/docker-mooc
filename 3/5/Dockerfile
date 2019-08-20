FROM ubuntu as build-stage

RUN apt-get update && apt-get install -y curl bash git && \
    curl -sL https://deb.nodesource.com/setup_10.x | bash && \
    apt-get install -y nodejs && \
    git clone https://github.com/docker-hy/frontend-example-docker.git && \
    mv frontend-example-docker app && \
    cd app && \
    npm install && \
    npm run build


FROM alpine

ENV API_URL=http://localhost:8000

COPY --from=build-stage /app/dist/ /app/dist/

RUN apk update && \
    apk add ca-certificates && \
    apk add --no-cache --repository http://dl-cdn.alpinelinux.org/alpine/v3.7/main/ nodejs=8.9.3-r1 && \
    npm install -g serve && \
    adduser -D app && \
    chown -R app:app /app

WORKDIR /app

USER app

CMD ["serve", "-s", "-l", "5000", "dist"]
