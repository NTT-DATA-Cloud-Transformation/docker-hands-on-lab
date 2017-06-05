First, lets run a single container from the command line as follows:

`docker run hello-world`{{execute}}

Docker downloaded an image of the container hello-world, started the container, ran a single command ("hello") and terminated the container. Lets try to understand what happenned. 

When the Docker engine received the command, it checked locally if the container image hello-world existed. Since it did not exist, it internally triggerred an action to pull the image. For reference, you can manually trigger image pulls using `docker pull hello-world`{{execute}}. It then ran the image with the default command (specified when the image is build). This started a new container and ran the default command. Once the command completed, it exited the container. 

You can change the status of your container by running 

`docker ps`{{execute}}

You will NOT see any container because your container has existed. To list exited and running containers, run `docker ps -a`{{execute}}. 

You can also check which images are present on your local system by running:

`docker images`{{execute}}


Now let us dissect this image. The container image hello-world is hosted at [DockerHub hello-world page](https://hub.docker.com/_/hello-world/). This image has the following Dockerfile: 

`
FROM scratch
COPY hello /
CMD ["/hello"]
`{{copy}}

You can find the [ actual source here ](https://github.com/docker-library/hello-world/blob/master/hello-world/Dockerfile).


Lets start at the bottom and work our way up this file. The CMD is specifying that when this container is run, without a command specified, it runs the command /hello. How did /hello get there? It was copied in using the COPY command. The FROM command specifies that this container was built using `scratch` which is a special image for building brand new images. Note: Most image you will work with will NOT be built from scratch but build from a layer such as `ubuntu` or `coreos`. 

If you question where the fille hello was copied from, it was copied from the host where the image was being built. Hello must be in the folder from where `docker build` was called at the time the image was built. You will soon learn how to build your own images.


What happens when you run the container with a non-default command? `docker run hello-world ls`{{execute}} 

This command fails because ls is a not a known command inside this container. The image hello-world has one and only one file, hello and hence it does not support running any other commands.

