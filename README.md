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
  
### docker build -t <your choice image name> Dockerfile location ## Build an image by using a file name Dockerfile (. is local directory)
  
  #### FROM ubuntu
  #### RUN apt-get update
  #### RUN apt-get -y install wget
  #### RUN apt-get -y install curl
### docker run -it imageName ## Run container interactively 
### docker hisoty imangeid ## See what commands are executed inside container.
  
  
  

