FROM alpine

ENV API_URL=http://localhost:8000

RUN apk add --no-cache bash git && \
    apk add --no-cache --repository http://dl-cdn.alpinelinux.org/alpine/v3.7/main/ nodejs=8.9.3-r1 && \
    git clone https://github.com/docker-hy/frontend-example-docker.git && \
    mv frontend-example-docker app && \
    cd app && \
    npm install && \
    apk del git && \ 
    cd .. && \
    adduser -D app && \
    chown -R app:app /app

WORKDIR /app

USER app

CMD ["npm", "start"]
