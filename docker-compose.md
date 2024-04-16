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
