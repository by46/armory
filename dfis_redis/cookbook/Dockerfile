FROM docker.neg/alpine:3.3

MAINTAINER from www.newegg.com by benjamin <benjamin.c.yan@newegg.com>

RUN echo https://mirrors.tuna.tsinghua.edu.cn/alpine/v3.3/main > /etc/apk/repositories && \ 
	echo https://mirrors.tuna.tsinghua.edu.cn/alpine/v3.3/main >> /etc/apk/repositories


RUN apk update && \
	apk add python python-dev py-pip redis

RUN pip install -i https://pypi.tuna.tsinghua.edu.cn/simple supervisor==3.3.0

RUN mkdir -p /opt/celery/

RUN mkdir -p /opt/data/

ADD supervisord.conf redis.conf  /opt/celery/

WORKDIR /opt/celery/

CMD ["supervisord", "--configuration", "/opt/celery/supervisord.conf"]

