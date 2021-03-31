# SSL
cert.conf -> DNS.1 = localhost <br>
diğer dosyayla birlikte C:\xampp\apache\crt içine atılacak

C:\Windows\system32\drivers\etc\hosts <br>
127.0.0.1 localhost

# MYSQL
my.ini
3306 -> 8809

# XAMPP

C:\xampp\apache\conf\extra

\#\# localhost <br>
 <VirtualHost *:80> <br>
     DocumentRoot "C:/xampp/htdocs" <br>
     ServerName localhost <br>
     ServerAlias *localhost <br>
 \</VirtualHost> <br>
 
 <VirtualHost *:443> <br>
     DocumentRoot "C:/xampp/htdocs" <br>
     ServerName localhost <br>
     ServerAlias *.localhost <br>
     SSLEngine on <br>
     SSLCertificateFile "crt/localhost/server.crt" <br>
     SSLCertificateKeyFile "crt/localhost/server.key" <br>
 \</VirtualHost>
