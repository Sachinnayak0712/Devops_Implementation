Jenkins Setup in Docker Container
1) update the Linux
	yum update -y

2) to install docker 
	yum install docker -y

3) to start the docker services
	systemctl start docker

4) to Enable the docker services
	systemctl enable docker

5) To run jenkins server using docker image
	docker run -p 8080:8080 -p 50000:50000 jenkins/jenkins:lts


##### Not Mandatory #####
If we are restarting the Machine
6) How to check the docker all running containers
	docker ps -a
	docker ps 

7) to start the docker conatiner 
	docker start "container_id"

Password for jenkins
cat /var/jenkins_home/secrets/initialAdminPassword








uivz ocek mwfz nnuc
