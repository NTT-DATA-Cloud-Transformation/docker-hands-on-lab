# Docker Hand-on Lab


## Install

Follow the steps [ here ](https://docs.docker.com/engine/installation/) for your operating system.

## Running a single container

### Starting docker machine (for non-Linux machines)

`docker-machine start default`

`docker env default`

On BASH:
`val $(docker-machine env)`

### Running a container with default command

`docker run hello-world`

`CONTAINER ID        IMAGE                     COMMAND                  CREATED              STATUS                          PORTS                                                                                         NAMES
483d02ad8cda        hello-world               "/hello"                 35 seconds ago       Exited (0) 35 seconds ago                                                                                                     desperate_archimedes`

The Docker container started and ran a single command, the program "/hello." 

Visit the [DockerHub page](https://hub.docker.com/_/hello-world/) for hello-world to understand what happenned. 

### Running a container with specific command

You can specify what command you want the container to run.

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




### Run a container for a while

https://hub.docker.com/_/nginx/

`docker run nginx `

### Run a container in interactive mode

`docker run -it ubuntu bash`

## Run a full Application

While running a single container is useful, there is often need to run a full apllication consisting of multuple containers. In such cases, rather than running each container related to an application individually from the command line, we can "compose" a collection of containers and run/stop them with a single command. This is done via docker-compose. 

### docker-compose.yml

Which containers to run and how to connect them together is specified in docker-compose.yml. Lets review this [example docker-compose.yml](http://FILLMEIN).

### Run wordpress locally

To run this docker-compose stack locally, you can: 

`cd lab2`
`docker-compose up` 

You can then access the Wordpress admin page at IP of your container. You are unable to see it why? What port shall you be using?

## Docker-ize your own application

### Building an image

### Fixing the Dockerfile 

### Running your image
