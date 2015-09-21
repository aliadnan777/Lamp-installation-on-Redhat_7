# Lamp-installation-on-Redhat_7

open terminal and switch to root user

* `su -`

#### Apache installation

install httpd by using `yum`

* `yum install httpd`

start apache by using

* `systemctl start httpd.service`

To make the apache to start during the every boot

* `systemctl enable httpd.service`

for testing, open browser and type

* `httpd://localhost`

#### mysql installation

install MySql by using following command

* ` yum install mariadb mariadb-server`

start Mysql

* `systemctl start mariadb.service`

to start during the every boot
 
* `systemctl enable mariadb.service`
 
run following command to `set root password`, `remove root accounts`, `remove anonymous-user accounts`, `remove the test database`
 
* `mysql_secure_installation`

#### php installation

type following command in terminal for installing php

* `yum install php php-mysql`

restart apache now

* `systemctl restart httpd.service`

for testing php 

* `vi /var/www/html/info.php`

add somthing in `info.php` file, now open browser and type `httpd://localhost/info.php`


