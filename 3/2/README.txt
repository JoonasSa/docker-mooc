Build the docker image and run it with: 

docker run -it -v $(pwd)/videos:/videos <image-id>

Inside the docker container run:

export PATH=$PATH:$HOME/.local/bin

And then:

yle-dl <yle-arena-video-url> -o <output-file-name>

You can find the downloaded video files in the videos directory from the path you ran the docker container from.