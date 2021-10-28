# Ansible Playbooks

## Introduction

These configuration files are part of my project for She Code Africa Cloud School Cohort 2. The main project is in [this repository](https://github.com/Z11mm/sca-project-c2-app-api)

## Ansible Setup

To install Ansible, follow these steps:
* Access the Ansible VM instance using ssh:
    - `gcloud compute ssh <ansible-server-name>`
* Generate SSH keys:
    - `ssh-keygen`
* Copy the public key:
    - `sudo cat ~/.ssh/id_rsa.pub`
* Access the Jenkins VM instance using ssh. 
* Paste the public key within `~/.ssh/authorized_keys` folder:
    - `sudo vi /home/<username>/.ssh/authorized_keys`
* Confirm connection between the two instances:
    - `ssh <jenkins-instance-ip-address>`
* Run the following commands to install Ansible:

    * Update Repository by including the official project’s PPA <br>
     `sudo apt-get update` <br>
     `sudo apt-add-repository -y ppa:ansible/ansible` <br>
     `sudo apt-get update` to refresh the package manager <br>

    * Install Ansible (and Python) <br>
     `sudo apt-get install -y ansible` <br>
     `sudo apt install python-pip -y` <br>

    * Install Boto Framework <br>
     `sudo pip install boto boto3` <br>
     `sudo apt-get install python-boto -y` <br>

    * Check that Ansible is installed <br>
     `ansible --version` <br>

    * Add the ip address of the target server to the Ansible's inventory file: <br>
     `sudo vi /etc/ansible/hosts` <br>