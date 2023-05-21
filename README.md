# setupTLBB
vi /etc/ssh/sshd_config
# line 43: change ( prohibit root login )
# for other options, there are [prohibit-password], [forced-commands-only]
PermitRootLogin yes
nhấn Phím Esc sau bấm phím i
trỏ mũi tên di chuyển để chỉnh
sau đó bấm nút Esc tiếp theo bấm :wq rồi enter
sau gõ reboot

sudo systemctl reload ssh
sudo systemctl restart sshd
sudo ufw disable
sudo apt-get update
sudo apt-get upgrade
sudo apt install aptitude -y
sudo dpkg --add-architecture i386
sudo apt-get update
sudo apt-get install libmysqlclient-dev -y
sudo apt-get install unixodbc -y
sudo apt-get install unixodbc-dev -y
sudo apt-get install libc6-i386 libc6-dev-i386 -y
sudo aptitude install libc6-i386 gcc-multilib libstdc++6:i386 libgcc1:i386 libcurl4-gnutls-dev:i386 -y
sudo apt-get install libstdc++6
sudo aptitude install unixodbc:i386 -y
sudo aptitude install wget -y
sudo apt-get update -y
sudo apt-get install -y lsb-release
sudo apt-get install -y lsb-core -y

Before we start, let’s make sure your system is up-to-date by running the following commands:

apt-get update
apt-get upgrade
Installing MariaDB on Ubuntu 21.10
apt-get install mariadb-server
Once the installation is complete, the MariaDB service will be started automatically. To verify if the service is running on your system, you can run the following command:

systemctl status mariadb

+ Chạy lệnh 
systemctl start mariadb
systemctl enable mariadb

+ Chạy lệnh 
systemctl status mariadb
 xem đã hiện active chưa

sudo ufw allow mysql

+ Chạy lệnh mysql_secure_installation
-cài đặt mật khẩu cho MySQL, nếu bị báo socket=/data/var/lib/mysql/mysql.sock 
chạy lệnh systemctl restart mariadb
 Chạy lệnh trên nó sẽ hiện ra thông báo "Enter current password for root enter for none" thì để trống bấm enter
 Thông báo kế bấm y, rồi set pass cho MySQL.
Sau đó các thông báo kế tiếp bấm theo như sau y,n,y,y


+ Chạy lệnh mysql -u root -p
Để mở MySQL
   GRANT ALL ON . TO root@'%' IDENTIFIED BY '123456';
   flush privileges;
 exit;
systemctl restart mariadb

+ Dùng navicat, kết nối đến MySQL, tạo 2 thư mục database tên là tlbb và web

sudo apt install nginx
sudo ufw app list
sudo ufw allow 'Nginx HTTP'
sudo systemctl enable nginx
sudo systemctl start nginx
sudo systemctl restart nginx
