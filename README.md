# docker

## Docker commands
docker pull: `docker pull <image-name>`
docker run: `docker run nginx`
docker run ububtu with sleep: `docker run ubuntu sleep 5`
docker run detach: `docker run -d <image-name>`
docker attach container: `docker attach <container-id>`
docker execute command on running container: `docker exec <container-id-or-name> <command>`
docker list container: `docker ps -a`
docker list images: `docker images`
docker stop: `docker stop <container-id-or-name>`
docker remove container: `docker rm <container-id-or-name>`
docker remove images: `docker rmi <image-name>`
