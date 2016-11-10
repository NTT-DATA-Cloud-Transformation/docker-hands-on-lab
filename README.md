# Docker Hand-on Lab


## Install

Follow the steps [ here ](https://docs.docker.com/engine/installation/) for you\
r operating system.

## Running a single container

### Running a container with default command

`docker run hello-world`

`CONTAINER ID        IMAGE                     COMMAND                  CREATED              STATUS                          PORTS                                                                                         NAMES
483d02ad8cda        hello-world               "/hello"                 35 seconds ago       Exited (0) 35 seconds ago                                                                                                     desperate_archimedes`

The Docker container started and ran a single command, the program "/hello." 

Visit the [DockerHub page](https://hub.docker.com/_/hello-world/) for hello-world to understand what happenned. 

### Running a container with specific command

`docker run busybox whoami`

`docker ps`

`docker run busybox ls`

`docker ps -a`

`CONTAINER ID        IMAGE                     COMMAND                  CREATED             STATUS                      PORTS                                                                                         NAMES
3f352d5d4412        busybox                   "whoami"                 31 seconds ago      Exited (0) 29 seconds ago                                                                                                 serene_elion
a1896d86beeb        busybox                   "ls"                     39 seconds ago      Exited (0) 37 seconds ago                       `                                                             
### Listing the Docker images you have downloaded so far

`docker images`
`REPOSITORY                TAG                 IMAGE ID            CREATED             SIZE
busybox                   latest              47bcc53f74dc        7 months ago        1.113 MB`

### Run a container in interactive mode


### Run a container for a while

`docker run wordpress`

## Run a full Application

### docker-compose.yml

### Run wordpress locally

`cd wordpress`
Run `docker-compose up` 

## Docker-ize your own application

### Building an image

### Fixing the Dockerfile 

### Running your image
