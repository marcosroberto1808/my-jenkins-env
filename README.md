# my-jenkins-env
Jenkins infrastructure to run pipelines
## Setup the docker image

docker build -t my-jenkins-env-image .

list instaled images: 

docker images -a
## Run the project

docker run --name my-jenkins-env-container -p 8080:8080 -p 50000:50000 -d my-jenkins-env-image 

## Get the initial Jenkins Admin Password
docker exec -it my-jenkins-env-container cat /var/jenkins_home/secrets/initialAdminPassword

## Useful commands
### list running containers

docker ps -a

### stop the container

docker stop my-jenkins-env-container

### remove the container 

docker rm my-jenkins-env-container
