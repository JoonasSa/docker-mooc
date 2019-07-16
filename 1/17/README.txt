To use the Python3 environment container first build it by running 'docker build . -t python3-env' or download it from DockerHub by running 'docker pull joonassa/python3-env-hy'.

Run a python3 file in the current directory from the host machine by running:
    'docker run -v $(pwd):/usr/src/app joonassa/python3-env-hy <file-name.py>'.

Use the container as a python3 repl by running: 
    'docker create -it --name python3-container joonassa/python3-env-hy'
    'docker start python3-container'
    'docker exec -it python3-container bash'

    Inside the container run 'python3'.