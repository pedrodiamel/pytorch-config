
## Install with docker

        docker build -f "Dockerfile" -t pytcv:latest .
        docker run \
                -ti \
                --privileged \
                --ipc=host \
                --name pytcv_project \
                -p 8888:8888 \
                -p 8889:8889 \
                -v $HOME/code:/workspace \
                -v $HOME/.datasets:/.datasets \
                pytcv:latest \
                /bin/bash

        docker run \
                -ti \
                --privileged \
                --ipc=host \
                --name pytcv_project \
                -p 8888:8888 \
                -p 8889:8889 \
                -v $HOME/code:/workspace \
                -v $HOME/.datasets:/.datasets \
                pytcv:latest \
                /bin/bash

## run

        jupyter notebook --port 8888 --allow-root --ip 0.0.0.0 --no-browser
        visdom -port 8889
