# mywebsite-jenkins
Jenkins infrastructure to run mywebsite app
## Setup the docker image

docker build -t mywebsite-jenkins-image .

list instaled images: 

docker images -a
## Run the project

docker run --name mywebsite-jenkins-container -p 8080:8080 -p 50000:50000 -d mywebsite-jenkins-image 

## Get the initial Jenkins Admin Password
docker exec -it mywebsite-jenkins-container cat /var/jenkins_home/secrets/initialAdminPassword

## Useful commands
### list running containers

docker ps -a

### stop the container

docker stop mywebsite-jenkins-container

### remove the container 

docker rm mywebsite-jenkins-container
