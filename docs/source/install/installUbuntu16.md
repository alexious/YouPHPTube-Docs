**This Tutorial will teach you how to install YouPHPTube Streamer Site what means it is the front end of YouPHPTube. You can watch it running at https://demo.youphptube.com/ or https://tutorials.youphptube.com/**

### If for any reason you need help to set up the YouPHPTube app or the server, fell free to ask us for help:
### https://www.youphptube.com/services

Just copy and paste this:

if you want to install both (encoder and streamer) use this compiled code:

`sudo apt-get install apache2 php7.0 libapache2-mod-php7.0 php7.0-mysql php7.0-curl php7.0-gd php7.0-intl mysql-server mysql-client ffmpeg git libimage-exiftool-perl && cd /var/www/html && sudo git clone https://github.com/DanielnetoDotCom/YouPHPTube.git && cd /var/www/html && sudo git clone https://github.com/DanielnetoDotCom/YouPHPTube-Encoder.git && sudo apt-get install python && sudo curl -L https://yt-dl.org/downloads/latest/youtube-dl -o /usr/local/bin/youtube-dl && sudo chmod a+rx /usr/local/bin/youtube-dl && sudo a2enmod rewrite`

or if you want just the encoder use this:

`sudo apt-get install apache2 php7.0 libapache2-mod-php7.0 php7.0-mysql php7.0-curl php7.0-gd php7.0-intl mysql-server mysql-client git && cd /var/www/html && sudo git clone https://github.com/DanielnetoDotCom/YouPHPTube.git`

or folowing the instructions

**LAMP** is short for **L**inux, **A**pache, **M**ySQL, **P**HP. This tutorial shows how you can install an Apache web server on an Ubuntu 16.x server with PHP 7 (mod_php) and MySQL. A LAMP setup is a perfect basis for your YouPHPTube.

**FFmpeg** is a free software project that produces libraries and programs for handling multimedia data. FFmpeg includes libavcodec, an audio/video codec library used by several other projects, libavformat (Lavf), an audio/video container mux and demux library, and the ffmpeg command line program for transcoding multimedia files.

**Git** is a version control system (VCS) for tracking changes in computer files and coordinating work on those files among multiple people.

To install LAMP and Git just open a terminal and type the following line:

`sudo apt-get install apache2 php7.0 libapache2-mod-php7.0 php7.0-mysql php7.0-curl php7.0-gd php7.0-intl mysql-server mysql-client git`

after all installations are complete type this command line:

`cd /var/www/html && sudo git clone https://github.com/DanielnetoDotCom/YouPHPTube.git`

##### Rewrite-modules

This is a important step.

We need to allow Apache to read .htaccess files located under the directory. You can do this by editing the Apache configuration file:

Find the section `<directory /var/www/html>` and change **AllowOverride None** to **AllowOverride All**

    sudo nano /etc/apache2/apache2.conf

After editing the above file your code should be like this:

    <Directory /var/www/>
              Options Indexes FollowSymLinks
              AllowOverride All
              Require all granted
      </Directory>

In order to use mod_rewrite you can type the following command in the terminal:

    sudo a2enmod rewrite

Restart apache2 after

    sudo /etc/init.d/apache2 restart

or

    sudo service apache2 restart

**The Encoder**

We recommend that you use an YouPHPTube Encoder privately, it is also available for free and open source and you can download it [here](https://github.com/DanielnetoDotCom/YouPHPTube-Encoder) and also we made some [installation instructions](https://github.com/DanielnetoDotCom/YouPHPTube-Encoder/wiki/How-to-install-LAMP,--FFMPEG-and-Git-on-a-fresh-Ubuntu-16.x---For-YouPHPTube-Encoder). But if you are limited in hardware or software resources feel free to use our public encoder https://encoder.youphptube.com/

We hope you have fun!
If you need help, have any question or Issue please open an Issue on [https://github.com/DanielnetoDotCom/YouPHPTube/issues](https://github.com/DanielnetoDotCom/YouPHPTube/issues)