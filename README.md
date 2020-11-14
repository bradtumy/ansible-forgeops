# ansible-forgeops


## Prerequisites
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
* You can run this playbook like this:  ansible-playbook -i ./hosts start_forgeops_install.yml
