#Update yum
yum install epel-release -y
yum update -y

#Apachec server install on centos

yum update httpd
yum install httpd -y  //install apache

#Enable, check, and start/stop services 

systemctl enable httpd
systemctl status httpd
systemctl start httpd
systemctl stop httpd
systemctl restart httpd

#Allow on firewall for http and https access

firewall-cmd --permanent --add-service=http
firewall-cmd --permanent --add-service=https
firewall-cmd --reload

# After installation check on browser

#PHP installation

yum install epel-release
yum install yum-utils
yum install http://rpms.remirepo.net/enterprise/remi-release-7.rpm
yum-config-manager --enable remi-php72

yum install php72
yum install php72-php-fpm php72-php-gd php72-php-json php72-php-mbstring php72-php-mysqlnd php72-php-xml php72-php-xmlrpc php72-php-opcache

php -v // check version of php


#MySQL install

#go the site and download latest repo of mysql
https://dev.mysql.com/downloads/repo/yum/
curl -sSLO https://dev.mysql.com/get/mysql80-community-release-el7-5.noarch.rpm
md5sum mysql80-community-release-el7-5.noarch.rpm  //verify with md5sum
rpm -ivh mysql80-community-release-el7-5.noarch.rpm // install package


yum install mysql-server // install mysql

#MySQL service start/stop

systemctl start mysqld
systemctl status mysqld
systemctl stop mysqld
systemctl enable mysqld

## Find default password for Mysql

grep 'temporary password' /var/log/mysqld.log


## Configure MySQL

mysql_secure_installation

mysqladmin -u root -p version  //check version

mysql -u root -p //login 



