# Comandos-usados-en-SO3-Adrian-Alcantara-Modulo-4
video 1 

sudo dnf install httpd -y

sudo systemctl start httpd

sudo systemctl enable httpd

sudo systemctl status httpd

sudo firewall-cmd --permanent --add-port=80/tcp

sudo firewall-cmd --reload

sudo mkdir -p /var/www/html/hola

echo "<h1>Hola Mundo</h1>" | sudo tee /var/www/html/hola/index.html

sudo nano /etc/httpd/conf.d/hola.conf

<VirtualHost *:80>
    ServerName hola.local
    DocumentRoot /var/www/html/hola
</VirtualHost>

sudo systemctl restart httpd

curl http://localhost

sudo mkdir -p /var/www/html/ariel
echo "<h1>Ariel Acevedo - 20251234 - Sistemas Operativos 3</h1>" | sudo tee /var/www/html/ariel/index.html

sudo nano /etc/httpd/conf.d/ariel.conf

Listen 8080
<VirtualHost *:8080>
    ServerName ariel.local
    DocumentRoot /var/www/html/ariel
</VirtualHost>



sudo firewall-cmd --permanent --add-port=8080/tcp
sudo firewall-cmd --reload


sudo systemctl restart httpd

curl http://localhost:8080




video 3

dnf install cups cups-pdf

systemctl start cups

systemctl enable cups

systemctl status 

Nano /etc/cups/cupsd.conf

Cupsctl --remote-admin

Usermod -aG sys nombre

Firewall-cmd --permanent --add-port=631/tcp

Firewall -cmd --reload

Systemctl restart cups

