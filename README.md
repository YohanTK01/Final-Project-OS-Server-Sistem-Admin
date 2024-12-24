# Final Project OS Server & Sistem Admin
- Nama  : Yohanes Yusuf Christolic
- NIM   : 23.83.0989
- Judul : Web Server Build Hero Mobile Legends
## Spesifikasi Server
- Ubuntu Server 24.04.01
- Ram 4 GB
- Prosesor 2 Core
- Storage 50 GB
## Deskripsi
- Saya memiliki ide untuk membuat web site yang nanti akan berisikan tips & trick dalam bermain game Mobile Legends: Bang Bang
- Fokus saya adalah membuat website yang akan memberikan rekomendasi build hero yang dapat digunakan oleh pemain pemula
- Untuk membuat websitenya saya akan mengunakan WordPress

## layanan yang digunakan
- Apache
- MariaDB
- PHP
- Postfix
- Varnish
  
## Langkah-langkah Instalasi

### 1. Memperbaharui paket Ubuntu
      sudo apt update && apt upgrade
   
### 2. Installasi Apache
#### a. Install Apache
      sudo apt install apache2

#### b. Mengaktifkan Firewall
      sudo ufw enable

#### c. Menyesuaikan Firewall untuk Apache
##### Buka daftar profil aplikasi UFW
      sudo ufw app list
##### Mengizinkan Apache pada port 80
      sudo ufw allow 'Apache'
##### Memverifikasi perubahan firewall
      sudo ufw status

#### d. Memverifikasi Server Web Anda
##### Memastikan Apache sudah berjalan
      sudo systemctl status apache2
##### Cek IP Server
      hostname -I
##### Mengecek Server Web di Browser
      http://your_server_ip
   
### 3. Installasi MariaDB
#### a. Install MariaDB
      sudo apt install mariadb-server
#### b. Mengkonfigurasi MariaDB
      sudo mysql_secure_installation
#### c. Menciptakan Pengguna Administratif yang Menggunakan Autentikasi Sandi
##### Membuka prompt MariaDB
      sudo mariadb
##### Mengubah nama pengguna dan kata sandi agar sesuai dengan preferensi Anda
      GRANT ALL ON *.* TO 'admin'@'localhost' IDENTIFIED BY 'password' WITH GRANT OPTION;
##### Membersihkan privilese untuk memastikan bahwa pengguna itu sudah disimpan dan tersedia di sesi ini
      FLUSH PRIVILEGES;
#### d. Menguji MariaDB
##### Memastikan MariaDB sudah berjalan
      sudo systemctl status mariadb
   
### 5. Installasi PHPMyAdmin
#### Install PHPMyAdmin
      sudo apt install phpmyadmin php-mbstring php-zip php-gd php-json php-curl
#### Mengaktifkan ekstensi PHP mbstring
      sudo phpenmod mbstring
   
### 6. Installasi Postfix
#### Install Postfix
      sudo DEBIAN_PRIORITY=low apt install postfix 
    
### 7. Installasi Varnish
      sudo apt install varnish
      
    
