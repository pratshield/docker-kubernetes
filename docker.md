# Docker
## What is Docker?
Docker is a open source software platform used to create, run and deploy virtualized application containers.

## Install Docker
Follow the installation guide [Get Docker](https://docs.docker.com/get-docker/)

## Docker CLI cheat sheet
### Info
- ```docker info``` Display system information
- ```docker version``` Display the system version
- ```docker login``` Login to Docker Registry

### Running containers
- ```docker pull <imageName>``` Pull an image from docker registry
- ```docker run <imageName>``` Run containers
- ```docker run -d <imageName>``` Run containers in detached mode
- ```docker start <containerName>``` Start stopped container
- ```docker ps``` List all running containers
- ```docker ps -a``` List all running and stopped containers
- ```docker stop <containerName>``` Stop running container
- ```docker kill <containerName>``` Kill containers
- ```docker image inspect <imageName>``` Get image info

### Attach shell
- ```docker run -it nginx -- /bin/bash``` Attach shell
- ```docker run -it -- microsoft/powershell:nanoserver pwsh.exe``` Attach powershell
- ```docker exec -it <containerName> --bash``` Attach to a running container

### Clean up containers
- ```docker rm <containerName>``` Removes stopped containers
- ```docker rm $(docker ps -a -q)``` Removes all stopped containers
- ```docker images``` List down all images
- ```docker rmi <imageName>``` Deletes the images
- ```docker system prune -a``` Removes all images not being used by any containers 
    
