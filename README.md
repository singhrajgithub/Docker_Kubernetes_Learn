# Docker_Learn

# Docker Architecture 
1) Client server based architecture , where Docker client act as client and Docker Daemon act as server.
2) Client is responsible for all inputs.
3) Docker Deamon responsible for running of the commands.
4) Daemon responsible for managing containers, images and pushing images to registries.
 
 
 ![DockerArchitecture](https://user-images.githubusercontent.com/24280813/155869228-35d8f5f9-8b14-4069-98a2-c0342a2536b0.JPG)
 
 # Why Docker is a Necessity
 1) Standardized Packaging -- same packaging for all types of applications i.e. Java , Python , JS.
 2) Multi Platform Support -- local machine , Cloud ,data center.
 3) Lightweight and Isolation -- containers are lightweight compared to VMs and are isolated from one another.
 4) Docker Deployment Architecture 

![Why_Docker](https://user-images.githubusercontent.com/24280813/155869456-9d3cc361-5e51-4be1-87b0-0445ed7ff591.JPG)

![Docker_Deployment](https://user-images.githubusercontent.com/24280813/155869518-4d442d59-57ea-432c-9c8c-08e549abd5bd.JPG)

# Useful Docker Commands 

1) docker images
2) docker container ls
3) docker ps -aq
4) docker container remove [container ID]
5) docker build -t hello-python:0.0.1.rel . [ build docker image locally for python application]
6) docker run -p 5000:5000 -d hello-python:0.0.1.rel [ image name : release name]
7) docker container prune -a
8) docker container rm 3e657ae9bd16
9) docker container ls -a
10) docker container pause 832
11) docker container unpause 832
12) docker container stop 832
13) docker container inspect ff521fa58db3
14) docker container prune
15) docker system
16) docker system df
17) docker system info
18) docker system prune -a
19) docker top 9009722eac4d
20) docker stats 9009722eac4d
21) docker --version
22) docker run -p 5000:5000 hello-world-python:0.0.1.RELEASE
23) docker run -p 5000:5000 hello-world-nodejs:0.0.1.RELEASE
24) docker logs 04e52ff9270f5810eefe1f77222852dc1461c22440d4
25) docker logs c2ba
26) docker images
27) docker container ls
28) docker container ls -a
29) docker container stop f708b7ee1a8b
30) docker run -d -p 5001:8080 hello-world-rest-api:0.0.1.RELEASE
31) docker pull mysql
32) docker search mysql
33) docker image history hello-world-java:0.0.1.RELEASE
34) docker image history 100229ba687e
35) docker image inspect 100229ba687e
36) docker image remove mysql
37) docker image remove hello-world-java:0.0.1.RELEASE
38) docker container rm 3e657ae9bd16
39) docker build -t rajsingh90/hello-node:0.0.1.rel .  --> creating nodejs image locally 
40) docker run -p 5001:5000 -d rajsingh90/hello-node:0.0.1.rel  --> running nodejs container with tag rajsingh90
41) docker push rajsingh90/hello-python:0.0.1.rel
42) docker network ls
43) docker network inspect bridge
44) docker stop [ container name] 
45) 


# Creating Efficient Docker Images
1) Moving steps up which are not changing or doesnot impact on any image file.

for example :
FROM node:8.16.1-alpine <br>
WORKDIR /app   <br>
COPY . /app  <br>
RUN npm install  <br>
EXPOSE 5000  <br>
CMD node index.js  <br>

Instead of copying whole codebase in step2 we can copy the package.json file which is not going to change very often . This will improve the performance of image creation time. Same thing can be done for python , java etc as well.

FROM node:8.16.1-alpine <br> 
WORKDIR /app  <br>
COPY package.json /app  <br>
RUN npm install  <br>
EXPOSE 5000  <br>
COPY . /app  <br>
CMD node index.js  <br>

# ENTRYPOINT VS CMD

1) CMD --> Command Line arguments will override the CMD in dockerfile and hence your application might not start.
2) ENTRYPOINT --> It can not be overridden via command line parameter however you can overridden by passing argument --entrypoint via cmd. It's quite complex to override the entrypoints although.

# How to configure environment variable to solve connection problem of localhost where two containers on bridged network cannot connect with each other.
1) use --env flag to configure 
2) use --link to configure the link

# How to use custom Networking connect microservices 

1) Host --> When we select host then container won't have it's own network and will work directly on host network itself. Host networking option works on Linux Hosts , it doesnot work on docker desktop for windows and mac etc.
2) none Network --> Means no netowkring at all.
3) Bridge Network --> already present
4) CreateCustom Network --> we can create custom network for our need. We can use **docker network create [Network name]** 

Command to use custom network while running 
docker run -d -p [exposed port : Docker Port] --name=[container Name] --network=[network name]

