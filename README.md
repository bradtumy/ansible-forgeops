# ansible-forgeops


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

## Usage 
* You can run these playbooks like this:  
```bash
ansible-playbook -i ./hosts start_forgeops_install.yml
```
```bash
ansible-playbook -i ./hosts destroy_forgeops.yml
```
