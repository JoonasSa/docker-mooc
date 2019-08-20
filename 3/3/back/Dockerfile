FROM ubuntu

ENV FRONT_URL=http://localhost:5000

RUN apt-get update && apt-get install -y curl bash git && \
    curl -sL https://deb.nodesource.com/setup_10.x | bash && \
    apt-get install -y nodejs && \
    git clone https://github.com/docker-hy/backend-example-docker.git && \
    mv backend-example-docker app && \
    cd app && \
    npm install && \
    # slim down the image
    apt-get purge -y --auto-remove curl git && \ 
    rm -rf /var/lib/apt/lists/* && \
    cd .. && \  
    useradd -ms /bin/bash app && \
    chown -R app:app /app

WORKDIR /app

USER app

CMD ["npm", "start"]
