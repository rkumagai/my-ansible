# my-ansible

```
$ a all -m ping -u vagrant -i hosts -vvvv 
```


# Remote host setting (Ubuntu)

@todo make task following.

```
// Create ansible user
$ sudo useradd -m ansible

// Password setting
$ sudo passwd ansible
Enter new UNIX password: ******
Retype new UNIX password: ******

// Change default shell to bash
$ sudo chsh -s /bin/bash ansible

// Add sudo to ansible
$ sudo update-alternatives --config editor
$ sudo visudo -f /etc/sudoers.d/ansible
ansible   ALL=(ALL) NOPASSWD: ALL

// Setting ssh login
$ sudo su - ansible
$ mkdir ~/.ssh
$ vim ~/.ssh/authorized_keys
$ chmod 700 ~/.ssh
$ chmod 700 ~/.ssh/authorized_keys

```


# Install roles by ansible-galaxy

```
ansible-galaxy install -r install_roles.yml
```

# Sites

- How To Install Solr 5.2.1 on Ubuntu 14.04
https://www.digitalocean.com/community/tutorials/how-to-install-solr-5-2-1-on-ubuntu-14-04

- apt - Manages apt-packages 
http://docs.ansible.com/ansible/apt_module.html

- Ansible roles
https://galaxy.ansible.com



