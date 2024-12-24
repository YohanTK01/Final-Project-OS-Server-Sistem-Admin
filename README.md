# Final Project OS Server & Sistem Admin
## Spesifikasi
1. Ram 8 GB
2. CPU 4 Core
3. Storage 50 GB
## Menentukan Ide
- Saya memiliki ide untuk membuat web site yang nanti akan berisikan tips & trick dalam bermain game Mobile Legends: Bang Bang
- Fokus saya adalah membuat website yang akan memberikan rekomendasi build hero yang dapat digunakan oleh pemain pemula
- Untuk membuat websitenya saya akan mengunakan WordPress
## Langkah-langkah Instalasi

### 1. Memperbaharui paket
      sudo apt update && apt upgrade
   
### 2. Install Apache
      sudo apt install apache2

#### Mengaktifkan Firewall
      sudo ufw enable

#### Menyesuaikan Firewall untuk Apache
      sudo ufw app list
      sudo ufw allow 'Apache'
      sudo ufw status

#### Memeriksa Server Web Anda
      sudo systemctl status apache2
      hostname -I
#### Mengecek Server Web di Browser
      http://your_server_ip
   
### 3. Install MariaDB
      sudo apt install mariadb-server
      sudo mysql_secure_installation
   
### 5. Install PHPMyAdmin
      $ sudo apt install phpmyadmin php-mbstring php-zip php-gd php-json php-curl
   
### 6. Install Postfix
      sudo DEBIAN_PRIORITY=low apt install postfix 
    
### 7. Install Caching
      sudo apt install varnish
    
