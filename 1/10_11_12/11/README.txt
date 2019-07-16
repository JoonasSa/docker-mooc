For the Dockerfile to work you need to clone https://github.com/docker-hy/backend-example-docker to the same directory.

After building the image you can run the container by running: 'docker run -d -p 8000:8000 -v $(pwd)/logs.txt:/logs.txt <id-of-image>'.
