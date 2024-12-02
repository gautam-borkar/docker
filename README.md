# docker

## Docker commands
docker pull: `docker pull <image-name>`
docker run: `docker run nginx`
docker run with version: `docker run <image-name>:<version>`
docker run with input and prompt: `docker run -it <image-name>`
docker run ububtu with sleep: `docker run ubuntu sleep 5`
docker rum map port: `docker run -p <docker-host-port>:<docker-container-port> <image-name>
docker run mount volume: `docker run -v <volume-location>:<dockr-container-location> <image-name>
docker run detach: `docker run -d <image-name>`
docker get layer detail: `docker history <image-name>`
docker attach container: `docker attach <container-id>`
docker execute command on running container: `docker exec <container-id-or-name> <command>`
docker list container: `docker ps -a`
docker list images: `docker images`
docker inspect cotainer: `docker inspect <container-name-id>`
docker cotainer logs: `docker logs <container-name-id>`
docker stop: `docker stop <container-id-or-name>`
docker remove container: `docker rm <container-id-or-name>`
docker remove images: `docker rmi <image-name>`

## Dockerfile
```
FROM ubuntu

RUN apt-get update && apt-get -y install python

RUN pip install flask flask-mysql

COPY . /opt/source-code

ENTRYPOINT FLASK_APP=/opt/source-code/app.py flas run
```