# Docker Hand-on Lab

This tutorial can be run via [ a web-based console ](https://www.katacoda.com/flux7/scenarios/lab) or locally. For the web-based console, visit [ https://www.katacoda.com/flux7/scenarios/lab ](https://www.katacoda.com/flux7/scenarios/lab). To run it locally, follow the following instructions. 

## Running Locally

### Install Docker

Follow the steps [ here ](https://docs.docker.com/engine/installation/) for your operating system.

### Starting docker machine

`docker-machine start default`

`docker env default`

On BASH:
`eval $(docker-machine env)`

Now follow the steps in the lab folder. 


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
