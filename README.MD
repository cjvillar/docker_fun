# Experimenting  With Docker

Build the Docker Images in each dir:
```bash
docker build -t <dir_name> .
```
Run the containers:

```bash
docker run -it <image_name>
```

## Cheatsheet [link_to_pdf](https://docs.docker.com/get-started/docker_cheatsheet.pdf)

Start the docker daemon:
```bash
docker -d
```
Get help with Docker:
```bash
docker --help
```
Build an Image from a Dockerfile:
```bash
docker build -t <image_name>
```
Build an Image from a Dockerfile without the cache:
```bash
docker build -t <image_name> . –no-cache
```
List local images:
```bash
docker images
```
Delete an Image:
```bash
docker rmi <image_name>
```
Remove all unused images:
```bash
docker image prune
```
Create and run a container from an image, with a custom name:
```bash
docker run --name <container_name> <image_name>
```
Run a container with and publish a container’s port(s) to the host:
```bash
docker run -p <host_port>:<container_port> <image_name>
```
Run a container in the background:
```bash
docker run -d <image_name>
```
Start or stop an existing container:
```bash
docker start|stop <container_name> (or <container-id>)
```
Remove a stopped container:
```bash
docker rm <container_name>
```
Open a shell inside a running container:
```bash
docker exec -it <container_name> sh
```
Fetch and follow the logs of a container:
```bash
docker logs -f <container_name>
```
To inspect a running container:
```bash
docker inspect <container_name> (or <container_id>)
```
To list currently running containers:
```bash
docker ps
```
List all docker containers (running and stopped):
```bash
docker ps --all
```
View resource usage stats:
```bash
docker container stats
```