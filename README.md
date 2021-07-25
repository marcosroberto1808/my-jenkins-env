# my-jenkins-env
Jenkins infrastructure to run pipelines
## Setup and run with docker-compose
docker-compose up -d --build
## Stop execution
docker-compose stop
## Get the initial Jenkins Admin Password
docker exec -it my-jenkins-env-container cat /var/jenkins_home/secrets/initialAdminPassword
## Useful commands
### list images
docker images -a
### list running containers
docker ps -a
### stop the container
docker stop my-jenkins-env-container
### remove the container 
docker rm my-jenkins-env-container
