# Ansible automation
A lab exercise for my Cloud Technologies class focused on automating the provisioning and configuration of an AWS infrastrucutre.
The project sets up 3 AWS instances, 2 configured with Nginx web servers and the other configured with HAProxy to act as a load balancer.
The load balancer uses the roundrobin algorithm.

# Usage
Clone this repo and run the command (with Ansible installed)
```
ansible-playbook -vv main.yml --ask-vault-pass
```
- This will require you to enter the Ansible Vault password below.

# Ansible Vault
Ansible Vault password: ansible

# Vars folder
Each vars folder contains an encrypted vars file (encrypted with Ansible Vault). These files specify the following variables:
- ec2_keypair: "ShanePersonalAWSKey" //Enter your own key here
- ec2_security_group: "sg-86787de0" //Enter your own security group
- ec2_instance_type: "t2.micro"
- ec2_image: "ami-a192bad2"
- ec2_subnet_ids: ["subnet-922bf6cb"] //Enter your own subnet here
- ec2_region: "eu-west-1"
- ec2_tag_Name: "HAProxy"
- ec2_tag_Type: "haproxy"
- ec2_tag_Environment: "production"
- ec2_volume_size: 8
- ec2_instance_count: 1 //Specifies how many instances to start

By Shane Lacey - 20013687
