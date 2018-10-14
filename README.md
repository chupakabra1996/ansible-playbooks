# ansible-ros-kinetic-playbook

ROS Kinetic installation playbook for Ubuntu 16.04 (Xenial) hosts.

## Prerequisites

To run the project you need (on your host machine):
- [`optional`] Vagrant
- Ansible (ver. 2+)
- [`optional`] Virtualbox
- SSH connection with the remote host (Ubuntu 16.04 Linux)

## Installaition

### Mac OS X

- Vagrant:
```shell
brew cask install vagrant
```

- Virtualbox:
```shell
brew cask install virtualbox
```

- Ansible:
```shell
brew install ansible
```

## Usage

- Start the virtual machine (VM):
```shell
vagrant up  # from the folder with Vagrantfile
```

- Provision the VM with `ansible` (using `vagrant`):
```shell
vagrant provision  # or vagrant up --provision
```

- Provision the VM or other host without `vagrant`:
```shell
ansible-playbook -i <inventory> provisioning/playbook.yml
```
See more on how to run playbooks with various parameters on ansible's [user guide](https://docs.ansible.com/ansible/2.5/user_guide/index.html).
