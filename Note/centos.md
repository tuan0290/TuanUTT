--Phân quyền cơ bản trên linux

---tạo user, và mật khẩu
	useradd tuan
	passwd tuan
---tạo group
	groupadd ketoan
	
--tọa thư mục
	mkdir ketoandata
	touch: tạo file
--phân quyền truy cập cho user ketoan vào thư mục ketoandata
	chown -Rf :ketoan ketoandata
--thêm user tuấn vào group ketoan
	usermod -a -G ketoan tuan
--phân quyền cho thư mục
	chmod -Rf 777 ketoandat

rm -Rf tuan : xóa thư mục
userdel tuan : delete user
groupdel tuan :delete group 

chown tuan:soi foder =>> user tuấn và group sói có quyền truy cập foder

- Một file & folder trong linux thì có 3 nhóm quyền
User, Group, Other

- Mỗi 1 nhóm thì có 3 quyền
Read, Write, Execute

- Bảng giá trị phân quyền
Number	Permission 	Type		Symbol
0		No Permission			---
1		Execute					--x
2		Write					-w-
3		Execute + Write			-wx
4		Read					r--
5		Read + Execute			r-x
6		Read +Write				rw-
7		Read + Write + Execute	rwx
-- tao apache
yum install -y httpd
systemctl start httpd
systemctl stop firewalld: tat tuong lua tam thoi
systemctl disable firewalld: tat tuong lua vinh vien
systemctl enable httpd.service : bat apache khi khoi dong lai auto 
--tao thu muc phan quen truy cao web
cd /var/www/html/
chown tuan-user:apache nguyenthanhtuan/ : phan quyen

vi index.html : tap index de test

vi /etc/httpd/conf/httpd.conf : coppy doan ma duoi vao vi nay

NameVirtualHost *:80

<VirtualHost *:80>
    ServerAdmin info@nguyenquocbao.info
    DocumentRoot /var/www/html/nguyenthanhtuan
    ServerName nguyenthanhtuan.info
    <Directory "/var/www/html/nguyenthanhtuan">      
   Order deny,allow
           Allow from all
           AllowOverride All
          Require all granted
   </Directory>
</VirtualHost>

systemctl restart httpd :khoi dong lai apache

Centos 8 install php multi version

1. Add remi repository
dnf -y install https://dl.fedoraproject.org/pub/epel/epel-release-latest-8.noarch.rpm

2. Remi install
dnf -y install https://rpms.remirepo.net/enterprise/remi-release-8.rpm

3. List php version
dnf module list php

4. Install php 7.3
dnf module install -y php:remi-7.3
dnf module install -y php:remi-7.4


5. Other package install
dnf install --enablerepo=remi php-mysqlnd
dnf install --enablerepo=remi php-gd
dnf install --enablerepo=remi php-xmlrpc
dnf install --enablerepo=remi php-pecl-mcrypt
dnf install --enablerepo=remi php-opcache
dnf install --enablerepo=remi php-pecl-apcu
dnf install --enablerepo=remi php-pecl-zip
dnf install --enablerepo=remi php-pear

6. Module mail install
pear install -a Mail

