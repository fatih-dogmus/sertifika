# SSL
cert.conf -> DNS.1 = localhost <br>
diğer dosyayla birlikte apache/crt içine atılacak

C:\Windows\system32\drivers\etc\hosts <br>
127.0.0.1 localhost

# MYSQL
my.ini
3306 -> 8809

# XAMPP
\#\# localhost
 <VirtualHost *:80>
     DocumentRoot "C:/xampp/htdocs"
     ServerName localhost
     ServerAlias *localhost
 </VirtualHost>
 <VirtualHost *:443>
     DocumentRoot "C:/xampp/htdocs"
     ServerName localhost
     ServerAlias *.localhost
     SSLEngine on
     SSLCertificateFile "crt/localhost/server.crt"
     SSLCertificateKeyFile "crt/localhost/server.key"
 </VirtualHost>
