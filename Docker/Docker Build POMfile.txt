1) Create a repo and commit the code with html file

2) Create Docket file in gethub repositiry
	Add the content 
# pull the tomcat docker image from docker hub
	FROM tomcat:latest

# person who is maintinag the docker file
	MAINTAINER "vnom1985@gmail.com"

# copying the the helloworld target war package from the target to destincation tomcat Container directory
	COPY ./target/helloworld-2.0-SNAPSHOT.war /usr/local/tomcat/webapps/

3) Install GIT and clone the repo
	Install GIT :- yum install git -y
	Clone the repo :- git clone 'repo_link'

4) Maven build
	yum install maven -y
	mvn -Dmaven.test.failure.ignore=true install
5) Build docker
	docker build -t "docker_image_name" .

6) Login docker
	docker login -u "username" -p "password"
	ex:
	      docker login -u sachinnayak0712 -p Sachinnayak@0712

7) Tag the image to account id
	docker tag "image_name" sachinnayak0712/image_name

8) Deploy in docker hub
	docker push vnom1985/project_vinod

 
