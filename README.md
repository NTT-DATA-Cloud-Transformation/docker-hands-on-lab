# Docker Hand-on Lab


## Install

Follow the steps [ here ](https://docs.docker.com/engine/installation/) for you\
r operating system.

## Running a single container

### Ephermal container

`docker run busybox whoami`

`docker ps`

`docker run busybox ls`

`docker ps -a`

`CONTAINER ID        IMAGE                     COMMAND                  CREATED             STATUS                      PORTS                                                                                         NAMES
3f352d5d4412        busybox                   "whoami"                 31 seconds ago      Exited (0) 29 seconds ago                                                                                                 serene_elion
a1896d86beeb        busybox                   "ls"                     39 seconds ago      Exited (0) 37 seconds ago                       `                                                             

`docker images`
`REPOSITORY                TAG                 IMAGE ID            CREATED             SIZE
busybox                   latest              47bcc53f74dc        7 months ago        1.113 MB`


dsfe
### Persistent service

`docker run nginx nginx -d`

### 
