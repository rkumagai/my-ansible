# my-ansible

# Check your hosts

```
$ a all -m ping -u vagrant -i hosts -vvvv 
```

# Create role skelton

```
$ mkdir -p roles/ansible_user/{tasks,handlers,templates,files,vars,meta}
$ echo "---" | tee roles/ansible_user/{tasks,handlers,vars,meta}/main.yml > /dev/null
```


# Install roles by ansible-galaxy

```
ansible-galaxy install -r install_roles.yml
```

---

# Vagrant setting

1. Create vagrant virtual server.

```
$ v init
// Here, modify Vagrantfile
$ v up
```

2. Setting ssh on your machine.

```
// Check virtual machine ssh config
$ v ssh-config

// Add following setting for auto login.
//
// Host {Your vagrant host name}
//  HostName     {Your vagrant host name}
//  User         vagrant
//  IdentityFile {Your vagrant idntify file}
$ vim ~/.ssh/config
```

3. Check if login virtual server with no password

```
$ ssh vagrant@{Your vagrant host name}
```

---

# Reference

- How To Install Solr 5.2.1 on Ubuntu 14.04
https://www.digitalocean.com/community/tutorials/how-to-install-solr-5-2-1-on-ubuntu-14-04

- apt - Manages apt-packages 
http://docs.ansible.com/ansible/apt_module.html

- Ansible roles
https://galaxy.ansible.com
https://galaxy.ansible.com/list#/roles?page=1&page_size=10



