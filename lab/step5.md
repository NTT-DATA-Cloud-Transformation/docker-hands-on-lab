While running a single container is useful, it is far more useful to be able to run multiple containers in tandem such that an entire application can be run. Docker makes this feature available through docker-compose. 

Analyze the following `docker-compose.yml` file. 

```
version: '2'

services:

  wordpress:
    image: wordpress
    ports:
      - 80:80
    environment:
      WORDPRESS_DB_PASSWORD: example

  mysql:
    image: mariadb
    environment:
      MYSQL_ROOT_PASSWORD: example
```

You can also get the contents from here: [https://github.com/Flux7Labs/docker-hands-on-lab/blob/master/lab/docker-compose.yml](https://github.com/Flux7Labs/docker-hands-on-lab/blob/master/lab/docker-compose.yml)

Now run this file as:
`docker-compose up -d`{{execute}}

