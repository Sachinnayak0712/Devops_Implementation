# How to to Install docker
	yum install docker -y

# To start the docker services
	systemctl start docker
	systemctl enable docker

# To Pull the images from Docker hub
	docker pull "imagename"

# To see the docker images
	docker images

# To see the docker container's running
	docker ps

# To see all the container running and other stopped container
	docker ps -a

# To run the docker images
	docker run "imagename"

# To start the conatainer
	docker start "container_id"

# To stop the conatainer
	docker stop "container_id"

# To remove the conatainer
	docker rm "container_id"

# To remove the docker image
	docker rmi "image_name"

# To remove all the Iamges
	docker rmi -f $(docker images -q)

# To stop all the container
	docker stop $(docker ps -q)

# To remove all conatiner
	docker rm $(docker ps -a -q)



# Content needed to add into Dockerfile
	FROM httpd:latest
	MAINTAINER nayaksachin0712@gmail.com
	COPY ./ /usr/local/apache2/htdocs/












