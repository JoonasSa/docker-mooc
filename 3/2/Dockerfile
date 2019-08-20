FROM ubuntu

RUN apt-get update && \
    apt-get install -y python3.6 python3-pip ffmpeg && \ 
    pip3 install --user --upgrade pycryptodome setuptools yle-dl && \
    rm -rf /var/lib/apt/lists/*

WORKDIR /videos

ENTRYPOINT ["/bin/bash"]
