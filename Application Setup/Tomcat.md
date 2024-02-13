Pre-Req
yum install java-11 -y

Install Tomcat

To download tomcat go to https://dlcdn.apache.org/tomcat/

1) Download Tomcat
           wget https://dlcdn.apache.org/tomcat/tomcat-8/v8.5.98/bin/apache-tomcat-8.5.98.tar.gz

2) Unzip the tomcat 
           tar -zvxf apache-tomcat-8.5.98.tar.gz

3) To start the services 
Go to
           cd /home/ec2-user/apache-tomcat-8.5.98/bin/
           ./startup.sh

Tomcat will run in default 8080 port number

4)By default the Manager is only accessible from a browser running on the same machine as Tomcat. 
If you wish to modify this restriction, you'll need to edit the Manager's context.xml file.

find / -name context.xml
Usually it will under 2 places, and it neeeds to be changed in both the places

          /home/ec2-user/apache-tomcat-8.5.98/webapps/host-manager/META-INF/context.xml
          /home/ec2-user/apache-tomcat-8.5.98/webapps/manager/META-INF/context.xml

	4A. Go to the path and To Edit the File with vi
                                   vi context.xml
	4B. Click on I from keyboard to make changes
	4C. Delete below lines
	               <Valve className="org.apache.catalina.valves.RemoteAddrValve"
	                 allow="127\.\d+\.\d+\.\d+|::1|0:0:0:0:0:0:0:1" />
	4D. To save and exit from vi 
	                press (ctlt + c )
	                :wq 

5) To start tomcat server
Go to bin folder
cd /home/ec2-user/apache-tomcat-8.5.98/bin/

./startup.sh 

To update the permssions if required
chmod +x startup.sh
chmod +x shutdown.sh


6) Update users information in the tomcat-users.xml file goto tomcat home directory and Add below users using vi tomcat-users.xml
	5A. Go to Path /home/ec2-user/apache-tomcat-8.5.98/conf/
		cd /home/ec2-user/apache-tomcat-8.5.98/conf/
	5B. Edit the file tomcat-users.xml
		vim tomcat-users.xml
	5C. Click on I from keyboard to make changes
	5D. Add the following user cred
		<role rolename="manager-gui"/>
		<role rolename="manager-script"/>
		<role rolename="manager-jmx"/>
		<role rolename="manager-status"/>
		<user username="admin" password="admin" roles="manager-gui, manager-script, manager-jmx, manager-status"/>
		<user username="deployer" password="deployer" roles="manager-script"/>
		<user username="tomcat" password="s3cret" roles="manager-gui"/>
	5E. To save and exit from vi
		press (ctlt+c)
		:wq

6) Will be succefully able to login to Tomcat Web Application Manager