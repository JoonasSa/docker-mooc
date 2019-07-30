FROM ubuntu
ENV API_URL=http://localhost:8000
EXPOSE 5000

RUN apt-get update && apt-get install -y curl bash git
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash && apt install -y nodejs

RUN git clone https://github.com/docker-hy/frontend-example-docker.git
RUN mv frontend-example-docker app

WORKDIR /app
RUN npm install

CMD ["npm", "start"]
