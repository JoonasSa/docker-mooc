FROM ubuntu
ENV FRONT_URL=http://localhost:5000
ENV REDIS=redis
ENV REDIS_PORT=6379
#EXPOSE 8000

RUN apt-get update && apt-get install -y curl bash git
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash && apt install -y nodejs

RUN git clone https://github.com/docker-hy/backend-example-docker.git
RUN mv backend-example-docker app

WORKDIR /app
RUN npm install

CMD ["npm", "start"]
