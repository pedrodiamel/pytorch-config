
## Install with docker

        docker build -f "Dockerfile" -t pytcv:latest .
        docker run \
                -ti \
                --privileged \
                --ipc=host \
                -v $HOME/code:/workspace \
                -v $HOME/.datasets:/.datasets \
                pytcv:latest \
                /bin/bash



        docker run \
                -ti \
                --privileged \
                --ipc=host \
                -v $HOME/code:/workspace \
                -v $HOME/.datasets:/.datasets \
                pytcv:latest \
                /bin/bash
