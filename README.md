
# Docker  

A handy guide to essential Docker commands for quick reference and efficient container management.  

---

## Docker Commands  

### Login to docker hub
```bash
docker login
```

### Pulling an Image  
```bash
docker pull <image-name>
```  

### Building an Image  
```bash
docker build . -t <account-name>/<image-name>
```  

### Pushing an Image
```bash
docker push <account-name>/<image-name>
```  

### Running a Container  
- Basic run:  
  ```bash
  docker run nginx
  ```  
- Run with a specific version:  
  ```bash
  docker run <image-name>:<version>
  ```  
- Run with interactive input and prompt:  
  ```bash
  docker run -it <image-name>
  ```  
- Run with a sleep command:  
  ```bash
  docker run ubuntu sleep 5
  ```  
- Run with environment variable:  
  ```bash
  docker run -e <env_name>:<env_value> <image_name>
  ```  

  ### Docker networks 
- **Deprecated**Run with link command
  ```bash
  docker run -d --link <hostname-in-application>:<container-name> <image-name>
  ```
- Run with network command
  ```bash
  docker network create my-network
  docker run --network my-network --name container1 <image1>
  ```

### Managing Ports and Volumes  
- Map host port to container port:  
  ```bash
  docker run -p <docker-host-port>:<docker-container-port> <image-name>
  ```  
- Mount a volume:  
  ```bash
  docker run -v <volume-location>:<docker-container-location> <image-name>
  ```  

### Container Management  
- Run in detached mode:  
  ```bash
  docker run -d <image-name>
  ```  
- Get image layer details:  
  ```bash
  docker history <image-name>
  ```  
- Attach to a running container:  
  ```bash
  docker attach <container-id>
  ```  
- Execute a command in a running container:  
  ```bash
  docker exec <container-id-or-name> <command>
  ```  

### Viewing and Inspecting  
- List all containers:  
  ```bash
  docker ps -a
  ```  
- List all images:  
  ```bash
  docker images
  ```  
- Inspect a container:  
  ```bash
  docker inspect <container-name-or-id>
  ```  
- View container logs:  
  ```bash
  docker logs <container-name-or-id>
  ```  

### Stopping and Removing  
- Stop a container:  
  ```bash
  docker stop <container-id-or-name>
  ```  
- Remove a container:  
  ```bash
  docker rm <container-id-or-name>
  ```  
- Remove an image:  
  ```bash
  docker rmi <image-name>
  ```  

---

## Docker compose

### Running docker compose
  - Run docker compose:
    ```bash
    docker-compose up
    ```  
---

## Docker registry

### Running docker registry locally
  - Running docker registry locally
    ```bash
    docker run -d -p 5000:5000 --name registry registry:2
    ```

### Push image to registry
  - Tag an image
    ```bash
    docker image tag <image-name> <tag-name>
    ```
  - Push image to registry:
    ```bash
    docker push <user-name>/<image-name>
    ```  
---

## Contributing  
Feel free to contribute by adding more commands or improving existing ones! Open a pull request or file an issue for any suggestions.  

---

## License  
This repository is licensed under the MIT License.  

---

**Happy Dockering!** 🚢
