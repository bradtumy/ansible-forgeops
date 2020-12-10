# ansible-forgeops

ForgeOps is a collection of ForgeRock resources to help you get started in the cloud. These resources demonstrate how to deploy the ForgeRock Identity Platform on Kubernetes. 

Use this playbook to have Ansible install forgeops on your local workstation where you have minikube running (or where you can install minikube).

## Prerequisites
Note: I have tried to install most of these libraries during the pre_tasks stage in this playbook.  At a minimum install Homebrew and Ansible yourself and then see if the playbook will install everything else.  I will update this note as I have the time to do more testing. YMMV.

On Host Machine: (e.g. your laptop)
* Install Homebrew - /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
* brew install ansible
* pip install openshift 


Install packages required by ForgeRock ()
- brew cask install docker
- brew cask install virtualbox
- brew install kubernetes-cli
- brew install skaffold
- brew install kustomize
- brew install kubectx 
- brew install minikube

## How to use
clone this repo to your localhost

## Customize the environment
Modify the inventory file "hosts" with the specific values for your enviroment.  You'll likely only need to change dev_home_dir and namespace.

## Usage 
You can run these playbooks like this:  
```bash
ansible-playbook -i ./hosts start_forgeops_install.yml
```
```bash
ansible-playbook -i ./hosts destroy_forgeops.yml
```

## Manual Configuration
Make sure you update your /etc/hosts with the ip from "minikube ip"
Output:
192.168.100.101

cat /etc/hosts
192.168.100.101 my-namespace.iam.example.com 

## Important Notes
* You may need to wait a few minutes for the services to finish starting before the console will load in a browser 

