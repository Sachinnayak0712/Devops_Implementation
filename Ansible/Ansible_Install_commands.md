# Installing Ansible 
	sudo yum update -y
	sudo yum install ansible -y

# Check the version		
	ansible --version

# How to run ansible shell command
# To check the ram utilization
	ansible all -i hosts -m shell -a "free -m"

To run ram utilization in project1 only
	ansible all -i ProjectA -m shell -a "free -m"

# To check the disk utilization
ansible all -i hosts -m shell -a "df -h"


# To check the disk utilization
	ansible all -i hosts -m shell -a "df -h"


# How to run ansible playbooks
	ansible-playbook -i "hosts" "file.yml"
	example :
		ansible-playbook -i hosts httpd_yum.yml
		ansible-playbook -i hosts docker.yml


Refer to documentation
https://docs.ansible.com/ansible/latest/collections/ansible/builtin/yum_module.html