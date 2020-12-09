# ansible-forgeops

ForgeOps is a collection of ForgeRock resources to help you get started in the cloud. These resources demonstrate how to deploy the ForgeRock Identity Platform on Kubernetes. 

Use this playbook to have Ansible install forgeops on your local workstation where you have minikube running (or where you can install minikube).

## Prerequisites

On Host Machine: (e.g. your laptop)
* Install Homebrew 
* pip install openshift 
* Install Ansible (brew install Ansible)
* Install packages required by ForgeRock:
- docker (cask)
- kubernetes-cli
- skaffold
- kustomize
- kubectx
- virtualbox (cask)
- minikube

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

