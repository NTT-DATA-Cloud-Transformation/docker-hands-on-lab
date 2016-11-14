We can also run images more interesting than hello-world which multiple files. One great examples is the `busybox` image. It is a great place to learn Docker as it contains the binaries of most common Linux command such as ls, echo, etc. Lets first pull the busybox image 

`docker pull busybox`{{execute}}

Now run a few commands to understand the image. 

`docker run busybox pwd `{{execute}}

This command will tell you that the commands you are are using `/` as the default working directory. This is another parameter we can set using the Dockerfile at the time of building the image. 

Lets see the contents of this working directory:
`docker run busybox ls`{{execute}}

You can ls other folder in the image, for example,
`docker run busybox ls /bin`{{execute}}

Now, try this: 
`docker run whoami`{{execute}}
`

The commands in busybox are run as root (the root inside the container) by default. 
