```
Hiển thị routing table :# route
In giá trị của các biến môi trường :# printenv
Khởi động lại máy : shutdown -r now
CPU info :# cat /proc/cpuinfo
Memory usage : # cat /proc/meminfo
Networking devices : cat /proc/net/dev
Kernel version : # cat /proc/version
Hiển thị thông tin về BIOS : # dmidecode -t 0
Xóa lịch sử : history -c
Hiện thị kernel modules hiện tại đang được load: lsmod
----
firewalld 
selinux
------
awk là:
Transform data files
Tạo ra các định dạng báo cáo

In toàn bộ file ra màn hình:

  awk '{print}' employee.txt
In các dòng có từ manager

  awk '/manager/ {print}' employee.txt 
Chi dòng ra làm nhiều cột, in cột thứ 1 và thứ 4 trong các dòng

  awk '{print $1,$4}' employee.txt
---
Cài đặt ntp(network time protocol) và cấu hình để cả server và client đều trỏ về một ntp server

yum install ntp -y
Chỉnh sửa file /etc/ntp.conf

server vn.pool.ntp.org iburst
Khởi động lại dịch vụ:

systemctl restart ntp.service 
Kiểm tra lại xem được chưa

ntpq -p
https://blogd.net/linux/cai-dat-va-cau-hinh-ntp-server-tren-linux/
---
 BWCTL (Bandwidth Test Controller) Bộ điều khiển kiểm tra băng thông
Server
Cài đặt bwctl-server

sudo apt-get update
sudo apt-get install bwctl-server -y
Client
sudo apt-get update
sudo apt-get install bwctl-client -y

https://github.com/trangnth/Report_Intern/blob/master/Linux-note/Command%20linux/bwctl.md
---
netstat là một công cụ command line để giám sát các kết nối mạng về cả incoming, outcoming
Lắng nghe tất cả các port (TCP và UDP) sử dụng netstat -a

Kiểm tra các port đang sử dụng phương thức TCP netstat -at

Kiểm tra các port đang sử dụng phương thức UDP netstat -au

Kiểm tra các port đang ở trạng thái listening netstat -l

Kiểm tra các port đang listen dùng phương thức TCP netstat -lt

Kiểm tra các port đang listen dùng phương thức UDP netstat -lu

Kiểm tra được port đang lắng nghe sử dụng dịch vụ gì netstat -plnt

Hiển thị bảng định tuyến netstat -rn

Kiểm tra những kết nối thông qua port 80 netstat -an | grep :80 | sort
----
ssh withou password
https://www.thegeekstuff.com/2008/11/3-steps-to-perform-ssh-login-without-password-using-ssh-keygen-ssh-copy-id/
ssh-keygen
ssh-copy-id -i ~/.ssh/id_rsa.pub remote-hostroo2
```