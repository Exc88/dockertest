Run the following commands:

#1. docker build --tag docker-last-test .
#2. docker run -p 8000:8000 docker-last-test

to reduce space:
docker build -t docker-gs-ping:<name1> -f Dockerfile.<name1> .

offline start:
docker run -d -p 8080:8080 docker-last-test

add name:
docker run -d -p 8080:8080 --name rest-server docker-gs-ping

delete all containers:
docker rm $(docker ps -a -q)