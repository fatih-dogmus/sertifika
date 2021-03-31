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
\tDocumentRoot "C:/xampp/htdocs" <br>
\tServerName localhost <br>
\tServerAlias *localhost <br>
 \</VirtualHost> <br>
 
 <VirtualHost *:443> <br>
\tDocumentRoot "C:/xampp/htdocs" <br>
\tServerName localhost <br>
\tServerAlias *.localhost <br>
\tSSLEngine on <br>
\tSSLCertificateFile "crt/localhost/server.crt" <br>
\tSSLCertificateKeyFile "crt/localhost/server.key" <br>
 \</VirtualHost>
