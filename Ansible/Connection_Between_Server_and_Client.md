# # Creating connection between Server and client

# 1) Create 1 server and desired no of client machine (ex: 3)

# 2) Go to Server machine
	How to use the password less authentication
		ssh-keygen
		(This will generate the key pair (id_rsa and id_rsa.pub) under .ssh) 
	
	Where to check my public key
		cd .ssh
		ls
		cat authorized_keys
		vi authorized_keys

# 3) We need to copy the id_rsa.pub key to the VM's/ machine which need to be connected- hosts unders - vi authorized_keys
	cd .ssh
	vi authorized_keys

# 4) To connect server and client
	command to connect from one linux machine to other linux machine through ssh
		ssh -i "private_key" user@ipaddress
		Example: ssh -i Demo_vinod_1Sep.pem ec2-user@3.89.74.234

# 		Once connected  then ssh should work without key
			ssh user@ipaddress
