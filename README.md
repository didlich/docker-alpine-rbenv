


# Commands

build:

    docker build -t alpine-rbenv --rm=true .


debug:

    docker run -i -t --entrypoint=sh alpine-rbenv


run:

    docker run -p 9000:9000 -e LOCAL_USER_ID=`id -u $USER` --name rbenv_instance -v ~/git:/home/user/git -i -P alpine-rbenv


login:

    docker exec -i -t -u user rbenv_instance /bin/bash


logout:

    exit