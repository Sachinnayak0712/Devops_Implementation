How to to Install docker
	yum install docker -y

to start the docker services
	systemctl start docker
	systemctl enable docker

to Pull the images from Docker hub
	docker pull "imagename"

to see the docker images
	docker images

to see the docker container's running
	docker ps

to see all the container running and other stopped container
	docker ps -a

to run the docker images
	docker run "imagename"

to start the conatainer
	docker start "container_id"

to stop the conatainer
	docker stop "container_id"

to remove the conatainer
docker rm "container_id"

to remove the docker image
	docker rmi "image_name"

to remove all the Iamges
	docker rmi -f $(docker images -q)

to stop all the container
	docker stop $(docker ps -q)

remove all conatiner
	docker rm $(docker ps -a -q)




FROM httpd:latest

MAINTAINER nayaksachin0712@gmail.com

COPY ./ /usr/local/apache2/htdocs/












