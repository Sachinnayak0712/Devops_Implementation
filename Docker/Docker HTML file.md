# 1) Create a repo and commit the code with html file

# 2) Create Docket file in gethub repositiry
	Add the content 
		FROM httpd:latest
		MAINTAINER "nayasachin0712@gmail.com
		COPT ./ /usr /local/apache2/htdocs/

# 3) Install GIT and clone the repo
	Install GIT :- yum install git -y
	Clone the repo :- git clone 'repo_link'

# 4) Navigate to the folder
	cd "file_name"

# 5) Build docker
	docker build -t "docker_image_name" .
Docker image will be created 

To directly run the image
	docker run -d -p 88:80  "docker_image_name"

# 6) Login docker
	docker login -u "username" -p "password"
	ex:
	      docker login -u sachinnayak0712 -p Sachinnayak@0712

# 7) Tag the image to account id
	docker tag "image_name" sachinnayak0712/image_name

# 8) Docker push
	docker push sachinnayak0712/image_name

 
