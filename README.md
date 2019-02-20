# Ansible Tower demo

Ansible Tower demo held at DORS/CLUC 2017 and Ansible Automates Tour Zagreb 2017.

Link to presentation: [Google Slides](https://docs.google.com/presentation/d/1II-tmWIaJS8vOUwBqz673aGIFTcU2-tYzKE2MuiswXE/edit?usp=sharing)

## Setup procedure

1. Make sure you have Vagrant and Ansible installed on your machine
1. Clone this git repository and position yourself in it
1. Generate SSH keypair for demo purposes `ssh-keygen -t rsa -N '' -f id_rsa`
1. Put private key in ansible-tower directory and public key in both ansible-tower and ansible-tower-clients directories
1. Modify Ansible variables (a.extra_vars) in Vagrant configuration files (Vagrantfile) if needed
1. Position yourself inside ansible-tower directory and run `vagrant up`
1. When the virtual machine is ready run `vagrant ssh`
1. Position yourself inside ansible-tower-clients directory and run `vagrant up`
1. [Download Go 1.11.5](https://dl.google.com/go/go1.11.5.linux-amd64.tar.gz) and put it in the web-infrastructure/files directory

### Note

Vagrant configuration files provided with this demo are using KVM as hypervisor for virtual machines. If you want to use different hypervisor you will need to modify Vagrant configuration files (Vagrantfile) located both in ansible-tower and ansible-tower-clients directories.

If you want to use some other Go version you need to modify Ansible group vars for webservers group (web-infrastructure/inventory/group_vars/webservers.yml) accordingly.
