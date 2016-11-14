Now we will learn how to build a new Docker image. The goal is to create a new image which displays "hello world" instead of the default nginx webpage we saw before. 

Create your Dockerfile for building your image by copying the contents below into the editor.

A file, index.html, has already been created for you and placed in the environment. Check that it is there:
`ls`{{execute}}

You can see its contents by running
`cat index.html`{{execute}}

Now add the following contents to your Dockerfile. 

`
FROM nginx
COPY index.html /usr/share/nginx/html
`

The first line is the base image, nginx in this case. The second list is copying the index.html file in the location where nginx looks for the index.html. 

Now build the image, 

`docker build -t webserver-image:v1 .`{{execute}}


Once the command completes, you can see your new image listed:
`docker images`{{execute}}

Now run the container using this image. You are expected to figure out what the command will be for this. 

Now figure out the steps to change the text displayed from Hello World to "I have got this" 

Stop and remove your container. 

