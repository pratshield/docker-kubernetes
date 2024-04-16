# Docker compose

docker compose is used to define and run multiple containers simultaneously

## docker compose use cases
- Workloads that don't require full orchestrator like Kubernetes
- For development and tests
- When we use services that can use docker compose files like AWS ECS, Azure App services, Virtual machines

## docker compose commands
- ```docker compose build``` Build the images
- ```docker compose start``` Start the containers
- ```docker compose stop``` Stop the containers
- ```docker compose up -d``` Build and start containers in detached mode
- ```docker compose ps``` List the running containers
- ```docker compose rm``` Remove all containers from memory
- ```docker compose down``` Stop and remove containers
- ```docker compose logs``` Get the logs
- ```docker compose exec <containerName> bash``` Run a command in a container

> ```docker-compose``` is docker version 01 and ```docker compose``` is docker version 02. Docker version 02 is faster than version 01

## docker compose version 02 commands
> It was not possible to run multiple instances of a docker compose in version 01 but it is possible in version 02

- ```docker compose -p <projectName> up -d``` Run an instance as a project
- ```docker compose ls``` List all running projects
- ```docker compose cp <containerID>:<src_path> <dest_path>``` Copy files from the container
- ```docker compose cp <src_path> <containerID>:<dest_path>``` Copy files to the container
- ```docker compose logs -f <containerName>``` Follow logs of the container
