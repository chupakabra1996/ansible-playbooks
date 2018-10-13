# ansible-ros-kinetic-playbook

ROS Kinetic installation playbook for Ubuntu 16.04 (Xenial).

## Prerequisites

To try this project you need (on your host):
- Vagrant
- Ansible (ver. 2+)
- Virtualbox

## Usage

- Start the virtual machine (VM):
```shell
vagrant up  # from the folder with Vagrantfile
```

- Provisioning the VM with ansible (using `vagrant`):
```shell
vagrant provision  # or vagrant up --provision
```

- Run the playbook on the remote host (without vagrant):
```shell
ansible-playbook -i <inventory> provisioning/playbook.yml
```
See more on how to run playbooks with various parameters on ansible's [user guide](https://docs.ansible.com/ansible/2.5/user_guide/index.html).

