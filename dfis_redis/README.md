# dfis_redis

该镜像用于celery的redis服务， 镜像已经预装了[supervisor 3.3.0](http://supervisord.org/)

## Pre-Install

1. [python 2.7.12-r0](https://www.python.org/)
2. python-dev 2.7.12.-r0
3. [freetds ](http://www.freetds.org/)
4. freetds-dev
5. pip 7.1.2-r0
6. [supervisor 3.3.0](http://www.supervisord.org/)

## Build Image
```shell
sudo docker build -t docker.neg/dfis_redis:0.0.1 .
```

## Run container
```shell

sudo docker run --name redis -dt -v /opt/redis:/opt/redis -p 6379:6379 docker.neg/dfis_redis:0.0.1

```