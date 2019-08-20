FROM ubuntu
ENV API_URL=http://localhost:8000

RUN apt-get update && apt-get install -y curl bash git && \
    curl -sL https://deb.nodesource.com/setup_10.x | bash && \
    apt-get install -y nodejs && \
    git clone https://github.com/docker-hy/frontend-example-docker.git && \
    mv frontend-example-docker app && \
    cd app && \
    npm install && \
    # slim down the image
    apt-get purge -y --auto-remove curl git && \ 
    rm -rf /var/lib/apt/lists/*

WORKDIR /app

CMD ["npm", "start"]
