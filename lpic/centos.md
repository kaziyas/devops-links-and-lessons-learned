# How to install CentOS 7.9 on a virtual machine

1.[ ] Download and install VMware Workstation Player | Pro from [here](https://www.vmware.com/products/workstation-pro.html).

2.[ ] Create a new virtual machine in the VMware workstation application.

3.[ ] Configure additional parameters for RAM, HDD, CPU, ...

4.[ ] A light CentOS Linux **ISO** can be downloaded from this [website](https://ftp.riken.jp/Linux/centos/7.9.2009/isos/x86_64/).

5.[ ] Imports the downloaded ISO into the virtual machine.

6.[ ] Set up a network adapter by following the instructions in this [link]( https://linuxhint.com/install_centos8_netboot_iso).
    > The first part of the instructions about creating a bootable flash drive can be skipped.

7.[ ] In the Software section, use the address https://mirror.23m.com/centos/7.9.2009/os/x86_64 .

8.[ ] The CentOS prompt will appear once you have created a root user and completed the remaining steps.

9.[ ] Connect to the installed operating system using the **Putty** application.

10.[ ] Once you have successfully logged into the OS, run the following command to install a few additional useful tools:
    ```
    yum -y install vim-common vim-enhanced bash-completion epel-release
    ```
11.[ ] You are now able to use the vim editor to create and edit the file

12.[ ] Use the following command to change the host name:
    ```
    hostnamectl set-hostname "devops"
    ```
    > There is additional information available [here](https://phoenixnap.com/kb/how-to-set-or-change-a-hostname-in-centos-7)