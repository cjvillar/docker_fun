# use the official Ubuntu base image from Docker Hub
FROM ubuntu:latest

#update package lists and install package 
RUN apt-get update && apt-get install -y nano && apt-get install -y screenfetch

# set a working directory inside the container
WORKDIR /app

# create or copy necessary files into the container
COPY . /app

# expose any necessary ports
# EXPOSE <port_number>

#Run a default command when the container starts, then run screenfetch
CMD ["/bin/bash"] 


