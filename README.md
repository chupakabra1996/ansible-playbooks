# ansible-ros-kinetic-playbook

ROS Kinetic installation playbook for Ubuntu 16.04 (Xenial) hosts.

## Getting started

### Prerequisites

To run the project you need (on your host machine):
- [`optional`] Vagrant
- Ansible (ver. 2+)
- [`optional`] Virtualbox
- SSH connection with the remote host (Ubuntu 16.04 Linux)

### Installaition

#### Ansible:

- Mac OS X:
```shell
brew install ansible
```
- Ubuntu 16.04:
```shell
sudo apt-add-repository ppa:ansible/ansible
sudo apt-get install ansible
```

### Usage examples

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

## Roles

- _common_:
  - Update and upgrade apt packages;
  - Install gcc and g++ from ubuntu-toolchains/test;
  - SublimeText installation.
- _ros_:
  - ROS Kinetic installation (desktop-full, ros-base, etc.);
  - Post-installation environment setup.
