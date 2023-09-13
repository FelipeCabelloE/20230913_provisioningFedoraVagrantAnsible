# Provisioning machines locally with Ansible and Vagrant

https://stribny.name/blog/provisioning-ansible-vagrant/

```sh
# The first thing that we have to do is to install Ansible, Vagrant and VirtualBox
sudo dnf install ansible vagrant VirtualBox -y 
```

```sh
# check if virtualization is enabled in BIOS
cat /proc/cpuinfo | egrep "vmx|svm"

# check if kernel module KVM is loaded
lsmod | grep kvm
```

```sh
sudo dnf install @virtualization
sudo systemctl start libvirtd

# to start the service on every boot
sudo systemctl enable libvirtd

```

```sh
# Add the desired box to vagrant

vagrant box add fedora/38-cloud-base
```

```sh
#init the box

vagrant init fedora/38-cloud-base
```

With the Vagrant configuration file in place, we can use some basic Vagrant commands to create and control the virtual machine:

**vagrant up** that will instruct Vagrant to create and run the virtual machine

**vagrant halt** that will stop the virtual machine

**vagrant destroy** that will destroy the virtual machine (useful when we change the VagrantFile and want to recreate it again)

**vagrant ssh** that will connect to that machine and give us a remote command line session

**vagrant ssh-config** that will display SSH connection information if we want to connect to the machine without Vagrant

```sh
#start the machine

vagrant up
```

```sh

```
