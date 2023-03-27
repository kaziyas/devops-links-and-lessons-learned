# How to install NGINX on CentOs
- [ ] As a first step, you should make sure that you do not have an installed version on the virtual machine through this command:
    ```
    systemctl status nginx
    ```
- [ ] In /etc/yum.repos.d/, locate nginx.repo file
    ```
    cd /etc/yum.repos.d/
    ls -a
    ```
- [ ] Use one of the following commands if this file cannot be found:
    ```
    vim /etc/yum.repos.d/nginx.repo
    vi /etc/yum.repos.d/nginx.repo
    ```
- [ ] Put the following contents into the file to set up the yum repository:
    ```
    [nginx-stable]
    name=nginx stable repo
    baseurl=http://nginx.org/packages/centos/$releasever/$basearch/
    gpgcheck=1
    enabled=1
    gpgkey=https://nginx.org/keys/nginx_signing.key
    module_hotfixes=true
    ```
- [ ] To install nginx, run the following command:
    ```
    yum -y install nginx
    ```
- [ ] Run the following command to make sure nginx is installed correctly:
    ```
    systemctl status nginx
    ```
- [ ] The following commands should be called sequentially to run and activate nginx:
    ```
    systemctl enable nginx
    systemctl start nginx
    ```
    <sub> 
    In the console, the $\color{green}{active [running]}$ in green indicates that nginx is installed and running
    </sub>

- [ ] The nginx message, **welcome to nginx**, should appear in the browser after disabling the firewall:   
    ```
    iptables -F
    systemctl disable --now firewalld
    ```
- [ ] Use the VM IP address in a browser to view the nginx message
    ```
    http://192.168.x.x:8080
    ```
<sub> 

There is additional information available on [nginx](http://nginx.org/en/linux_packages.html#RHEL) and [cyberciti](https://www.cyberciti.biz/faq/how-to-install-and-use-nginx-on-centos-7-rhel-7/)    

</sub> 
