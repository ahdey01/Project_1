## Documentation of project1

# update a list of packages in package manager
'sudo apt update'
![apt update](./images/Sudo apt update.png)

# apache2 package installation
'sudo apt install apache2'
![apache2 status](./images/apache2.png)

# apache2 verification status
'sudo systemctl status apache2'
![apache2 verification](./images/apache2 verification result.png)

# Try to check if we can access it locally in our Ubuntu shell
'curl http://localhost:80'
![EC2 config output](./images/EC2 configuration output.png)

# installing mysql
'sudo apt install mysql-server'
![mySQL server status](./images/mySQL server status.png)

# login to mysql
'sudo mysql'
![mysql login output](./images/mysql login output.png)

# installing mysql secure installation
'sudo mysql_secure_installation'
![interactive script installation](./images/interactive script installation.png)

# test login mysql output
'sudo mysql -p'
![Login mysql output](./images/Login mysql output.png)

# installing php
'sudo apt install php libapache2-mod-php php-mysql'
![php installation](./images/php installation.png)

# domain setup called projectlamp
'sudo mkdir /var/www/projectlamp' 
'sudo chown -R $USER:$USER /var/www/projectlamp'
'sudo vi /etc/apache2/sites-available/projectlamp.conf'
'<VirtualHost *:80>
    ServerName projectlamp
    ServerAlias www.projectlamp 
    ServerAdmin webmaster@localhost
    DocumentRoot /var/www/projectlamp
    ErrorLog ${APACHE_LOG_DIR}/error.log
    CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>'
'Hit the esc button on the keyboard
Type :
Type wq. w for write and q for quit
Hit ENTER to save the file'

# To show the new file in site available
'sudo ls /etc/apache2/sites-available'
![new file insite](./images/new file insite output.png)

# To enable the new virtual host
'sudo a2ensite projectlamp'
# To enable the new virtual host
'sudo a2dissite 000-default'
![enable/disable new virtual](./images/enable and disable new virtual host.png)
# To prevent syntax error
'sudo apache2ctl configtest'
'sudo systemctl reload apache2'

# Created a file named index.php
'vim /var/www/projectlamp/index.php'
'<?php'
'phpinfo();'
[php file output](./images/php file output.png)

