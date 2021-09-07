# ALX Training - Project Vagrant

*This project focuses mainly on setting up Vagrant and testing it*

## Why use Virtual Machines? And why Vagrant?

### My machine vs. virtual environments

Your computer’s environment - whether it’s Windows, MacOS or a Linux distribution - will change a lot over time, with or without you noticing. You will install applications, games, tools, … that will require and install different dependencies and at the end of the day you can end up having completely different behaviors or even have something not work because of software conflicts.

Using virtual environments prevents developers from these problems.

### The tools

There are multiple tools out there that can help you create and manage virtual environments (notice that we use the term “virtual environment” here, as such environemnt is not necessarily a VM. Technologies using containerization allow one to manage virtual environments as well).
We are using two tools: **VirtualBox** and **Vagrant**.

**VirtualBox** is a Virtual Machine provider. The virtual machines themselves will be spawned using VirtualBox. VirtualBox is free and lightweight, which make it a perfect choice for us.

**Vagrant** is a tool that sits on top of a VM provider. Again, we chose to use VirtualBox as a provider, but other providers exist out there and Vagrant offers the possibilty to use dfferent providers (More info here). Just like VirtualBox, we choose to use Vagrant because it is free, reliable and well maintained. Keep in mind that the purpose here is to use Virtual environments, and both VirtualBox and Vagrant are just means to achieve this purpose.

## How to install Vagrant on your personal computer

### Windows

* Download [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
* Install VirtualBox
* Download [Vagrant](https://www.vagrantup.com/downloads)
* Install Vagrant
* Open the command prompt
* Add the **Ubuntu 20.04** (`trusty64`) image to your box list

```
C:\Users\kidusmik> vagrant box add ubuntu/trusty64
```

* Create your first virtual machine:

```
C:\Users\kidusmik> vagrant init ubuntu/trusty64
```

This will generate a `Vagrantfile` with `base = "ubuntu/trusty64"` - *you don’t have to execute this command line everyday, only once, to create a new virtual machine*

```
C:\Users\kidusmik> vagrant plugin install vagrant-vbguest
```

This is to avoid issue with the lastest version of `Vagrant`.

```
C:\Users\kidusmik> vagrant up
```

This will start your virtual machine

```
C:\Users\kidusmik> vagrant ssh
```

Now you are inside your `virtual machine`.

```
vagrant@vagrant-ubuntu-trusty-64:~$
```
