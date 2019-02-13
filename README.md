
# Vagrant Box

This is a vagrant box designed for php developers,especially those who need to link Oracle and MSSQL.

The box includes CentOS 7, Apache web server 2.4.6, PHP 7.2.15 With extension such as sqlsrv,oci8..., MariaDb 5.5.6, Microsoft ODBC Driver 17 for SQL Server, Oracle instant client 12 12.2.0.1.0

# How To use

Install [Virtualbox](https://www.virtualbox.org/)

Install [Vagrant](https://www.vagrantup.com/)

The default VagrantFile setting is for windows users.
If you use Linux or Mac , please configure it yourself.

The default vagrant sync is slow , so we changed it to nfs type.
In order for it to work, we need to install the nfs tool for windows.

`vagrant plugin install vagrant-winnfsd`

Then we can make the box run.

`vagrant box add wakeasp/CentOS7PHP7`

`vagrant up` 

There is a defualt apache DocumentRoot sync to host directory  "C://web". 
If you want to change it, do it by yourself in the VagrantFile.

The default database root password is "root".