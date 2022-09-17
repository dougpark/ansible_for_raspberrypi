# Ansible for Raspberry Pi
Ansible is a tool to help you manage multiple Raspberry Pi's.

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

## More Information
* [GitHub - ansible/ansible: Ansible is a radically simple IT automation platform that makes your applications and systems easier to deploy and maintain. Automate everything from code deployment to network configuration to cloud management, in a language that approaches plain English, using SSH, with no agents to install on remote systems. https://docs.ansible.com.](https://github.com/ansible/ansible)
* [Jeff Geerling - Author and Software Developer in St. Louis, MO](https://www.jeffgeerling.com)
* [Teach, learn, and make with the Raspberry Pi Foundation](https://www.raspberrypi.org)
* [Visual Studio Code - Code Editing. Redefined](https://code.visualstudio.com)
* [How To Install the Latest Python Version on Raspberry Pi? | Raspberry tips](https://raspberrytips.com/install-latest-python-raspberry-pi/)
* [How To Check Which PIP Version Is Installed On Your System | Raspberry tips](https://raspberrytips.com/check-which-pip-version-is-installed/)
* [Use SSH To Remote Control Your Raspberry Pi: A complete guide | Raspberry tips](https://raspberrytips.com/ssh-guide-raspberry-pi/)
