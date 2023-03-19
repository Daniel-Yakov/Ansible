# Ansible
This Github repository contains an Ansible playbook and inventory files that demonstrate how to use Ansible to install Docker on EC2 instances. The playbook uses the inventory file to specify the target hosts where Docker needs to be installed.

The inventory file is a YAML file that defines the list of hosts and their corresponding attributes. In this case, the inventory file specifies the EC2 instances' IP addresses and the user for the ssh connection.

The Ansible playbook includes the necessary tasks to install Docker on the target EC2 instances. 

The playbook uses Ansible modules to perform these tasks. The modules used in the playbook include 'apt', 'apt_key', 'apt_repository', and 'shell'.

Check that ansible can establish ssh connection to the target machines:
```
ansible all -i inventory.yaml -m ping
```

Run the playbook:
```
ansible-playbook -i inventory.yaml playbook.yaml 
```

## Requirements
To use this Ansible playbook to install Docker on EC2 instances, you must meet the following requirements:

1. Ansible installed: You must have Ansible installed on the computer from where you plan to run the playbook. Ansible can be installed on a variety of operating systems, including Linux, macOS, and Windows. Refer to the Ansible documentation for installation instructions.

2. SSH access to target machines: You must have SSH access to the target EC2 instances where you want to install Docker. You should have SSH keys set up on the control machine and authorized on the target instances. It is recommended to add the SSH key to the ssh-agent for improved security and convenience.

3. You will need to specify the target machines' IP addresses in the inventory file



