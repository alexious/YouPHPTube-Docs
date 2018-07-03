# Install on Debian 9.3

This tutorial is from magicmissile72, you can find the very original
here: https://github.com/DanielnetoDotCom/YouPHPTube/issues/649

1. Install Debian 9.3 from net-install cd or dvd1
2. Select only 'ssh server' and 'common tools'
3. Finish install and secure/customize with any additional apps you need
   (like htop, vmware-tools, etc)
4. ssh in and configure IP and DNS
5. Install MariaDB 10.2 from the repository

``apt-get install software-properties-common dirmngr``

(wait for install to complete...)

``apt-key adv --recv-keys --keyserver keyserver.ubuntu.com 0xF1656F24C74CD1D8``

(wait for install to complete...)

``add-apt-repository 'deb [arch=amd64,i386,ppc64el] http://ftp.osuosl.org/pub/mariadb/repo/10.2/debian stretch main'``

``apt-get update``

``apt-get install mariadb-server``

6. MariaDB will ask for a password during install...so enter one
7. Run the 'secure install' for MySQL/MariaDB

``mysql_secure_installation``

8. Login to MariaDB

``mysql -u root -p``

9. Create the Main Database (youPHPTube)

``CREATE DATABASE youPHPTube;``
``CREATE USER 'youphptube'@'localhost' IDENTIFIED BY '---------------';``
``GRANT ALL PRIVILEGES ON youPHPTube.* TO youphptube@localhost;``
``FLUSH PRIVILEGES;``

10. Create the Encoder Database (youPHPTube-Encoder) note: no hyphen,
    Maria with barf on that...

``CREATE DATABASE youPHPTubeEncoder;``
``CREATE USER 'youphptubecoder'@'localhost' IDENTIFIED BY '---------------';``
``GRANT ALL PRIVILEGES ON youPHPTubeEncoder.* TO youphptubecoder@localhost;``
``FLUSH PRIVILEGES;``

quit;

11. Continue with main install script sans mysql (we installed that
    above) removed 'mysql-server mysql-client' from snippet use this
    instead...

``apt-get install curl apache2 php7.0 libapache2-mod-php7.0 php7.0-mysql \``
``php7.0-curl php7.0-gd php7.0-intl ffmpeg git libimage-exiftool-perl \``
``&& cd /var/www/html && sudo git clone https://github.com/DanielnetoDotCom/YouPHPTube.git \``
``&& cd /var/www/html && sudo git clone https://github.com/DanielnetoDotCom/YouPHPTube-Encoder.git \``
``&& sudo apt-get install python \``
``&& sudo curl -L https://yt-dl.org/downloads/latest/youtube-dl -o /usr/local/bin/youtube-dl \``
``&& sudo chmod a+rx /usr/local/bin/youtube-dl && sudo a2enmod rewrite``

note: should be all one line...

12. restart Apache systemctl restart apache2

13. Pre-configre YouPHPTube copy-n-paste the following in the CLI and
    wait... The 'cat' show command before and after as a sort of error
    checking...so you can see if it changed the value correctly. note: I
    need to make this into a shell script...

copy below and start pasting

``mkdir /var/www/html/YouPHPTube/videos``

``mkdir /var/www/html/YouPHPTube-Encoder/videos``

``chown -R www-data:www-data /var/www/html/YouPHPTube/``

``chmod 755 /var/www/html/YouPHPTube/videos``

``chown -R www-data:www-data /var/www/html/YouPHPTube-Encoder/``

``chmod 755 /var/www/html/YouPHPTube-Encoder/videos``

``cat /etc/php/7.0/apache2/php.ini | grep post_max_size``

``sed -i -e 's/post_max_size = 8M/post_max_size = 1000M/g' /etc/php/7.0/apache2/php.ini``

``cat /etc/php/7.0/apache2/php.ini | grep post_max_size``

``cat /etc/php/7.0/apache2/php.ini | grep upload_max_filesize``

``sed -i -e 's/upload_max_filesize = 2M/upload_max_filesize = 1000M/g' /etc/php/7.0/apache2/php.ini``

``cat /etc/php/7.0/apache2/php.ini | grep upload_max_filesize``

``cat /etc/php/7.0/apache2/php.ini | grep max_execution_time``

``sed -i -e 's/max_execution_time = 30/max_execution_time = 7200/g' /etc/php/7.0/apache2/php.ini``

``cat /etc/php/7.0/apache2/php.ini | grep max_execution_time``

``cat /etc/php/7.0/apache2/php.ini | grep memory_limit``

``sed -i -e 's/memory_limit = 128M/memory_limit = 512M/g' /etc/php/7.0/apache2/php.ini``

``cat /etc/php/7.0/apache2/php.ini | grep memory_limit``
``systemctl restart apache2``

End pasting

14. Edit Apache... **hint: edit line 172, change 'None' to 'all'**

``vi /etc/apache2/apache2.conf``

``<Directory /var/www/>`` ``Options Indexes FollowSymLinks``
``AllowOverride All`` ``Require all granted``

15. Restart Apache...

``systemctl restart apache2``

16. Go to your main site URL: /YouPHPTube/install
17. Go to your encoder site URL: /YouPHPTube-Encoder/install
18. Enjoy!
