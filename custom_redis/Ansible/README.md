# Ansible Classroom Environment
The official training environment for our ansible classes.

## Prerequisite Tools
* Virtualbox
* Vagrant
* Ansible

## Instructions for Use
1. Clone this directory.
2. Run '`vagrant up`' and wait for the VMs to spin up.
3. Run ansible commands from this directory.

### Notes for Windows Users
#### [**Ansible currently does not support running on windows as a control node.**](http://blog.rolpdog.com/2020/03/why-no-ansible-controller-for-windows.html)
So you will not be able to execute ansible commands directly from the powershell command line.

To use this training environment, please install the Ubuntu shell (WSL2) from the Microsoft Windows Store.
Once installed, you'll need to install the `sshpass` utility by running the following commands inside the Ubuntu shell.

#### Using the latest Virtualbox will prevent you from launching these vms.
Windows has decided that it won't let Virtualbox run while hyperV is running. (Which it will be if you're using WSL.)
The last known version of Virtualbox that works on Windows alongside WSL is [6.1.22](https://download.virtualbox.org/virtualbox/6.1.22/VirtualBox-6.1.22-144080-Win.exe).


```bash
$ sudo apt update
$ sudo apt install sshpass ansible
```

Once that's done, **you need to append `--ask-pass` to every ansible command we use** in the class.
The default password for these vms is `vagrant`.

## Verify if Things are Working
Simply run the following command to verify.
```bash
$ ansible all -m ping
```
