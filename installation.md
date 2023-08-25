# Update yum
yum install epel-release -y <br>
yum update -y

# Apachec server install on centos

yum update httpd <br>
yum install httpd -y  //install apache

# Enable, check, and start/stop Apache services 
systemctl enable httpd <br>
systemctl status httpd <br>
systemctl start httpd <br>
systemctl stop httpd <br>
systemctl restart httpd <br>

# Allow on firewall for http and https access

firewall-cmd --permanent --add-service=http <br>
firewall-cmd --permanent --add-service=https <br>
firewall-cmd --reload 

# After installation check on browser
![image](https://github.com/tagoremithun/Apache-MySQL-Php-Security/assets/15008622/bf0b4ee0-b600-4991-843d-3fe69db85958)

# PHP installation

yum install epel-release <br>
yum install yum-utils <br>
yum install http://rpms.remirepo.net/enterprise/remi-release-7.rpm <br>
yum-config-manager --enable remi-php72 <br> 

yum install php72 <br>
yum install php72-php-fpm php72-php-gd php72-php-json php72-php-mbstring php72-php-mysqlnd php72-php-xml php72-php-xmlrpc php72-php-opcache <br>

php -v // check version of php  <br>

![image](https://github.com/tagoremithun/Apache-MySQL-Php-Security/assets/15008622/5c24132b-1975-41da-8e28-5c5b63af608f)


# MySQL install
#go the site and download latest repo of mysql <br>
https://dev.mysql.com/downloads/repo/yum/ <br>
curl -sSLO https://dev.mysql.com/get/mysql80-community-release-el7-5.noarch.rpm <br>
md5sum mysql80-community-release-el7-5.noarch.rpm  //verify with md5sum <br>
rpm -ivh mysql80-community-release-el7-5.noarch.rpm // install package <br>

yum install mysql-server // install mysql

# MySQL service start/stop 

systemctl start mysqld <br>
systemctl status mysqld <br>
systemctl stop mysqld <br>
systemctl enable mysqld <br>

## Find default password for Mysql

grep 'temporary password' /var/log/mysqld.log <br>


## Configure MySQL

mysql_secure_installation <br>

mysqladmin -u root -p version  //check version <br>

mysql -u root -p //login <br>



