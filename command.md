docker run -it ubuntu:latest bash

cat /etc/lsb-release

docker run -it ubuntu sleep 3

docker run -it --rm ubuntu -c "sleep 3; echo job finished"

docker attach

docker exec

docker cp test.txt hardcore_mendeleev:/root/

docker logs

docker port

docker run -itd --rm -p 111 ubuntu:14.04 bash

docker run -it --rm --name server ubuntu:14.04 bash

docker run -it --rm --link server --name client ubuntu:14.04 bash

docker network create 

docker run -it --rm --net=x --name server ubuntu:14.04 bash

docker run -it --rm --link server --net=x --name client ubuntu:14.04 bash

docker save -o backup.tar.gz ubuntu debian

docker load -i backup.tar.gz

docker run -ti -v /home/..:/container_data ubuntu bash

docker run -ti --name pc1 -v /share ubuntu bash

docker run -ti --name pc2 --volumes-from pc1 ubuntu bash

```
FROM ubuntu:14.04

MAINTAINER 1RT <1rt.buivantri@gmail.com>

RUN <command>

ADD data.txt /data.txt

ENV HTTPS_PORT=443

ENTRYPOINT start
CMD end-1st

SHELL cat data.txt
EXEC ["/cel" ,"xxx"]

EXPOSE 8080

VOLUME ["xxx"]

USER 1amtr
```

docker build -t demo:v1.0 .