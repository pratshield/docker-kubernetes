# Volumes

## Persisting data in containers
**Containers are short-lived and stateless**
We usually don't store data in containers. We usually write data in containers which we don't want to keep because when the containers are destroyed, all data is lost

To persist data, we need to store the data outside of containers, in volumes.

Volumes maps a folder on the host to a logical folder in the container.

## Volumes commands cheat sheet
- ```docker create volume <volumeName>``` Creates a new volume
- ```docker volume ls``` List all volumes
- ```docker volumne inspect <volumeName>``` Display the volume info
- ```docker volume rm <volumeName>``` Deletes a volume
- ```docker volume prune``` Deletes all volumes not mounted
