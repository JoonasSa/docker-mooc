FROM alpine as build-stage

RUN apk update && \
    apk add git gcc musl-dev && \
    git clone https://github.com/JoonasSa/brainfuck_interpreter.git && \
    cd brainfuck_interpreter && \
    gcc -o bf main.c

FROM alpine

COPY --from=build-stage /brainfuck_interpreter/bf /app/bf

RUN apk update && \
    adduser -D app && \
    chown -R app:app /app

USER app

ENTRYPOINT [ "./app/bf" ]