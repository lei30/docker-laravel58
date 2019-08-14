# laravel58 docker

from https://www.digitalocean.com/community/tutorials/how-to-set-up-laravel-nginx-and-mysql-with-docker-compose

## local

```bash
$ docker-compose up -d

# goto localhost:8080

$ docker-compose down
```

## stage

```bash
# as root user
$ adduser www
$ usermod -aG sudo www && usermod -aG docker www
$ su - www && cd ......

$ docker-compose -f docker-compose-stage.yml -d up

# goto {IP}:8080

$ docker-compose -f docker-compose-stage.yml down
```
