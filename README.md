# Rozak-Lab-Web-Server
Install Apache
============
1. Install apache
         ```sudo apt install apache2```
2. Cek status apache 
        ```sudo systemctl status apache2```
3. Cek hostname
        ```hostname -I```
4. Ubah pemilik folder “/var/www/html” dari root ke www-data
        ```sudo chown -R www-data:www-data /var/www/html```
5. Beri ijin anggota grup untuk merubah folder “/var/www/html”
        ```sudo chmod -R g+rw /var/www/html```
6. Tambahkan user name kita ke grup www-data
        ```sudo usermod -a -G www-data [my username]```
7. Restart komputer
Langkah 8 dan 9 bisa di skip jika tidak menggunakan firewall
8. Tambahkan rule untuk apache di firewall
        ```sudo ufw allow 'Apache'```
9. Cek status firewall
        ```sudo ufw status```


MySQL
======
1. Install MySQL
        ```sudo apt install mysql-server```
2. Jalankan skrip keamanan untuk meningkatkan keamanan database
       `` sudo mysql_secure_installation```
3. Cek status MySQL
        ```sudo service mysql status```


PHP
====
1. Install PHP
        ```sudo apt install php libapache2-mod-php php-mysql```
