# Install_ansible
## Objective
After completing this activities you will be able to automate linux automation tasks with ansible.
Install ansible on a control node.
## Description
Automation avoid manual system administration and configuration. this allow administrator automate repetitive task
A good automation process is to write a programm, ideally in comprehensive language, to focus on critical things.
### What is ansible
Ansible is an open source automation platform. it's an automation engine that run ansible playbook.
Ansible is a poerful management automation platform to many workflow and envirenments.
Ansible playbook provide humain readable automation. it is easy for human to read, comprehend and change.
playbook execute task in order.
Ansible can be used to orchestrate the entire application productive quickly.
there are two machine in the ansible architecture: control node and manage node. control node is an  administration laptop
in which ansible will be install and run. 
list of the manage node are list on the inventory file. the inventory file can be defined in a static or dynamic text file.
A file that containt the task is call playbook. Each playbook life have an .yml extension
### Platform support: 
linux, Unix, Network device, cloud environment, virtualization, cointener environment
Antomation language: amsible playbook
### Installation process
Ansible is simply to install on a control node(workstation) in which ansible will be run.
Noted: the control node should only be Linux or Unix system. Microsoft Windows is not supported as a control node,
Although windows system can be managed hosts.
### Prerequis
Python 3 (3.6 or later) need to be installed on the control node
Ensure you already subscrib to red hat subscription manager or setup local repolist
#### install python
```
yum update
yum install epel-release -y
yum search python36
yum install python36 -y
alternatives --set python /usr/bin/python3
```
#### install python-pip
Different mode are available to install ansible
In this case you will install ansible with the help od python module pip
```
yum install python3-pip
```
#### Install Ansible
Use pip3 to install ansible
```
pip3 install ansible
```
#### Verify ansible installation
command use to verified ansible installation
```
ansible --version
```
### setup ansible configuration file
#### inventory file location
inventory is specified on ansible.cfg configuration file
if configuration is not setup 
you can create ansible.cfg on /etc/ansible/ repository
```
touch /etc/ansible/ansible.cfg
```
setting in ansible.cfg are organize in two section
1. fist section
```
[defaults]
inventory=/etc/myhost.txt
remote_user= root
host_key_checking=false
```
- defaults : set default setting
- inventory: specifies the path to the inventory file
- remote_user: is the name of the user that logs in on the remote hosts
- host_key_checking: specified whether or not to prompt for a password 
2. second section
```
[privilege_escalation]
become = True
become_method = sudo
become_user = root
become_ask_pass = False
```
- become : 



