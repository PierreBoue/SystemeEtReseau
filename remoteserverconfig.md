Updating the Debian Linux, run:
sudo -- sh -c 'apt update && apt upgrade'
Install Apache, execute:
sudo apt install apache2
Update the Firewall and open port 80 and 443, run:
sudo ufw allow in "WWW Full"
Set up MariaDB:
sudo apt install mariadb-server
Secure your MariaDB server, type:
sudo mysql_secure_installation
PHP 7.3 installation:
sudo apt install php libapache2-mod-php php-gd php-mysql
Test your LAMP setup
Let us see all steps in details. But, first log in to your remote server using the ssh command:
ssh user@server-ip
ssh -i ~/.ssh/aws-ec2-key admin@deb10-lmum1-box1

créer un nouvel utiloisateur mysql

mysql -u root -p -h localhost
I created a new user with

CREATE USER 'francesco'@'localhost' IDENTIFIED BY 'some_pass';
then I created the database

CREATE DATABASE shop;
I granted privileges for new user for this database

GRANT ALL PRIVILEGES ON shop.* TO 'francesco'@'localhost';


sudo nano /var/www/html/dbtest.php