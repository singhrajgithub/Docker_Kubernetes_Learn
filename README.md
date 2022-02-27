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
37) docker image remove in28min/hello-world-java:0.0.1.RELEASE
38) docker container rm 3e657ae9bd16
