
# Vagrant Box

This is a vagrant box designed for php developers,especially those who need to link Oracle and MSSQL.

The box includes CentOS 7, Apache web server 2.4.6, PHP 7.2.15 With extension such as sqlsrv,oci8..., MariaDb 5.5.6, Microsoft ODBC Driver 17 for SQL Server, Oracle instant client 12 12.2.0.1.0

# How to Set up

Install [Virtualbox](https://www.virtualbox.org/)

Install [Vagrant](https://www.vagrantup.com/)

The default VagrantFile setting is for windows users.
If you use Linux or Mac , please configure it yourself.

Then we can make the box run.

If you use the window OS ,you can install nfs plugin.

`vagrant plugin install vagrant-winnfsd`

`vagrant box add wakeasp/CentOS7PHP7`

`vagrant up` 

# How to use

There is a defualt apache DocumentRoot sync to host directory  "C://web". 
If you want to change it, do it by yourself in the VagrantFile.

The mariaDB users:

root@localhsot  password:root

vagrant@localhost password:root

The nfs sync have some problem on writing a large number of files .

If you use a framework as a symfony, put the cache, session, and log directories outside of the syn dir.

[How to Override Symfony's default Directory Structure](https://symfony.com/doc/current/configuration/override_dir_structure.html#override-cache-dir)

A folder (/Symfony) was originally set up. You can put them in.