# my-ansible

```
$ a all -m ping -u vagrant -i hosts -vvvv 
```


# Remote host setting (Ubuntu)

```
// Create ansible user
$ useradd ansible

// Password setting
$ sudo passwd ansible
Enter new UNIX password: ******
Retype new UNIX password: ******

// Change default shell to bash
$ sudo chsh -s /bin/bash

// Add sudo to ansible
sudo update-alternatives --config editor
sudo visudo -f /etc/sudoers.d/ansible

// Setting ssh login
$ sudo su - ansible
$ mkdir ~/.ssh
$ vim ~/.ssh/authorized_keys
```


# Sites

- How To Install Solr 5.2.1 on Ubuntu 14.04
https://www.digitalocean.com/community/tutorials/how-to-install-solr-5-2-1-on-ubuntu-14-04

- apt - Manages apt-packages 
http://docs.ansible.com/ansible/apt_module.html

- Ansible roles
https://galaxy.ansible.com



