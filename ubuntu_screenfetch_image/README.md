# Example Docker image based on Ubuntu:

```Dockerfile
# official Ubuntu base image from DockerHub
FROM ubuntu:latest

# update package lists and install a simple package 
RUN apt-get update && apt-get install -y nano 

# (Optional) Set a working directory inside the container
WORKDIR /app

# (Optional) Create or copy necessary files into the container
COPY . /app

# (Optional) Expose any necessary ports
# EXPOSE <port_number>

# (Optional) Define environment variables
# ENV key=value

# (Optional) Run a default command when the container starts
# CMD ["executable","param1","param2"]

# (Optional) Entrypoint configuration
# ENTRYPOINT ["executable", "param1", "param2"]

# (Optional) Define volume mount points for external storage
# VOLUME ["/data"]

# (Optional) User for the container
# USER <username>

# (Optional) Add metadata to the image
# LABEL version="1.0" description="My Ubuntu-based image"

# (Optional) Any additional configurations or commands required

# (Optional) Set default command to be executed when the container starts
CMD ["/bin/bash"]
```

## Explanation of the commands used:

- `FROM`: Specifies the base image to use (in this case, the latest Ubuntu image available on Docker Hub).
- `RUN`: Executes commands during the build process to install packages or perform specific tasks.
- `WORKDIR`: Sets the working directory inside the container.
- `COPY`: Copies files from the local directory (in the host machine) into the container.
- `EXPOSE`: Exposes specific ports from the container to the host machine.
- `ENV`: Sets environment variables inside the container.
- `CMD`: Specifies the default command to be executed when the container starts. In this case, it starts a bash shell.
- `ENTRYPOINT`: Defines the default executable for the container.
- `VOLUME`: Creates mount points for external volumes.
- `USER`: Sets the default user for the container.
- `LABEL`: Adds metadata to the image.

Save this code in a file named `Dockerfile` and build the Docker image using the `docker build` command. For example:

```bash
docker build -t my-ubuntu-image .
```

This command builds the Docker image using the Dockerfile in the current directory (`.`) and tags it as `my-ubuntu-image`. After the image is built, run a container from it using `docker run`:

```bash
docker run -it --rm my-ubuntu-image
```

This command starts a container from the `my-ubuntu-image` image, enters the interactive mode (`-it`), and removes the container once it stops (`--rm`).


### Notes:
The current image in this dir builds a container that shows:[screenfetch](https://www.cyberciti.biz/open-source/command-line-hacks/howto-display-linux-logo-in-bash-terminal-using-screenfetch-linux_logo/)

and is not a direct copy of the Dockerfile above.