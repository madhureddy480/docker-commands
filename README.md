# docker-commands
### sudo usermod -a -G docker $USER
### sudo service docker service
### docker version
### docker ps ## current running container
### docker ps -ls
### docker ps -a ## All container ran so far
### docker ps -l ## last ran container
### docker rm ## remove container
### docker rmi ## remove image
### docker rmi -f ## force remove image
### docker diff image1 image2 ## diff images
### docker commit containerid <image name> ## save chnages to docker image
  
### docker tag imageId <image name> ## naming an image
  
### docker build -t <your choice image name> Dockerfile folder ## Build an image by using a file name Dockerfile (. is local directory)
  
  #### FROM ubuntu
  #### RUN apt-get update
  #### RUN apt-get -y install wget
  #### RUN apt-get -y install curl
  #### CMD (17 video)
  #### ENTRYPOINT to pass our command in interactive mode (18,19 video)
  
### docker run -it imageName ## Run container interactively 
### docker hisoty imageid ## See what commands are executed inside container.
  
  
## override the entry point command
docker run -it --entrypoint bash imagename
  
## Running server on a port
#### step 1: download web server image
step 2 -run command: docker run -d -p 32456:8000 imageName  
###### -d is deamon -p is port
###### now the server is running on host port 32456 and tcp/ip port 8000
###### curl localhost:32456

## Docker container ip address
docker inspect --format '{{ .NetworkSettings.IPAddress }}' containerId
###### curl 172.0.72.2:8000

## Remove all docker containers
docker rm $(docker ps -a)
docker rm -f $(docker ps -a)
## Remove all docker images
docker rmi $(docker images)
docker rmi $(docker images -q)
docker rmi -f $(docker images -q)

