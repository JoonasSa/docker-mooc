FROM ubuntu
COPY . .
RUN apt-get update && apt-get install -y curl && apt-get install -y bash
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash && apt install -y nodejs && node -v && npm -v && npm install
CMD ["npm", "start"]
