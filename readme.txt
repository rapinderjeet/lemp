#!/bin/bash
service --status-all | grep '\[ + \]'

echo "Installation Start"
sudo apt update
apt upgrade -y

echo "nginx Start"
sudo apt install nginx -y
echo "nginx Finish"

echo "mysql-server Start"
apt install mysql-server -y
echo "mysql-server Finish"

echo "mysql-server Start"
apt install supervisor -y
echo "mysql-server Finish"
------------------------------------------------------------------
sudo add-apt-repository ppa:ondrej/php
echo "PHP install Start"
Apache2
sudo apt install php7.2 php7.2-cli php7.2-common -y
Nginx
sudo apt install php7.2-fpm -y
echo "PHP install Finish"
------------------------------------------------------------------
echo "PHP Extension Start"

apt install php7.2-curl php7.2-gd php7.2-json php7.2-mbstring php7.2-intl php7.2-mysql php7.2-xml php7.2-zip -y

// Updated
sudo apt install php7.2-curl php7.2-gd php7.2-intl php7.2-mbstring php7.2-mysql php7.2-xml php7.2-zip -y

sudo apt install php7.2-curl php7.2-xml php7.2-gd php7.2-intl php7.2-mbstring php7.2-mysql php7.2-xml php7.2-zip -y

sudo apt install php7.4-bcmath php7.4-curl php7.4-xml php7.4-gd php7.4-imap php7.4-intl php7.4-mysql php7.4-soap php7.4-xml -y

sudo apt install php7.4-zip php7.4-xmlrpc php7.4-mbstring php7.4-imagick

sudo apt install php7.2-curl php7.2-xml php7.2-gd php7.2-intl php7.2-mbstring php7.2-mysql php7.2-zip -y

sudo apt install php7.2-bcmath
sudo apt install php7.2-imap
sudo apt install php7.2-soap 
sudo apt install php7.2-pgsql
sudo apt install php7.2-xsl
sudo apt install openssl
sudo apt install php7.2-memcached
sudo apt install php7.2-common

sudo apt install php8.0-curl php8.0-xml php8.0-gd php8.0-intl php8.0-mbstring php8.0-mysql php8.0-zip -y

echo "PHP Extensions Finish"
------------------------------------------------------------------

echo "composer Start"
apt install composer -y
echo "composer Finish"

echo "git Start"
apt install git -y
echo "git Finish"

systemctl enable nginx

echo "Installation Finish"

check certificates
check es and mysql ip white lists

sudo cp cert.crt /usr/local/share/ca-certificates/
sudo cp sh-es.crt /usr/local/share/ca-certificates/
sudo update-ca-certificates
------------------------------------------------------------------
Redis Install:
sudo apt install redis-server -y
sudo nano /etc/redis/redis.conf
sudo systemctl restart redis.service
sudo systemctl status redis
redis-cli
------------------------------------------------------------------
sudo apt install memcached
------------------------------------------------------------------
Server migrate check list:
nginx
php7.2 fpm
supervisor
cron

nginx config
php7.2 config
supervisor config
cron config
migrate code

Remove old server.
Check all server if IP is used.
