# Ansible for Raspberry Pi

## Special Thanks
* Jeff Geerling for his Ansible book and YouTube video series
* [Ansible 101 YouTube series | Jeff Geerling](https://www.jeffgeerling.com/project/ansible-101-youtube-series)
* [Ansible for DevOps](https://www.ansiblefordevops.com)
* YouTube playlist [Ansible 101](https://www.youtube.com/playlist?list=PL2_OBreMn7FqZkvMYt6ATmgC0KAGGJNAN)

## Step 1 - Install Ansible
* Install python3
* Install pip3
* pip install ansible
* For more information read Jeff's book

## Step 2 - Create ansible.cfg
* Steps for basic ansible working dir
```
mkdir ansible
cd ansible
touch ansible.cfg
code ansible.cfg
```
* Create inventory file
```
touch inventory
code inventory
```
* Base ansible.cfg file
* Tell ansible where to find inventory file
```
[defaults]
INVENTORY = inventory
```

## Step 3 - Create inventory
* The inventory file contains a list of hosts that you want to work with ansible
* You can us IP address or name
* You must have ssh access
* Preferably have a common login id
* In my case I use pi, which is noted here

```
[local]
frodo.local

[all]
frodo.local
link.local
solo.local
pihole.local
zelda.local

[all:vars]
ansible_user=pi
```

## Step 4 - Run your first ad-hoc command
* This command will return the memory space for all hosts listed in the ```[all]``` section of the inventory file
```
ansible all -a "free -m"
```

## Step 5 - Create a Playbook

## Step 6 - Run your first Playbook

