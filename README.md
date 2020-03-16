# Ansible Installation

To install ansible please follow below mention commands
```
$ sudo apt update
$ sudo apt install software-properties-common
$ sudo apt-add-repository --yes --update ppa:ansible/ansible
$ sudo apt install ansible

```
# Nexus Installation

First thing you have edit ansible.cfg file.Inside ansible.cfg you need define "remote_user" 
and "private_key_file".Follow below mention command and example value

```
$ sudo nano ansible.cfg 
```
Example:-
```
remote_user = "ubuntu"
private_key_file = Openwitclub.pem
```
After config ansible.cfg .Follow below mention command to excute ansible playbook.In "<Public_DNS>" 
adding your aws ec2 instance public dns value ex:-("ec2-18-232-76-22.compute-1.amazonaws.com") 
```
$ ansible-playbook -i <Public_DNS>, jenkins.yml
```
Example :-
```
$ ansible-playbook -i ec2-18-232-76-22.compute-1.amazonaws.com, jenkins.yml
```
