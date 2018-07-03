Create AWS S3
=============

**Details:** \* Only videos will be saved on S3, all images will be
saved locally. \* Dummy video with 10 bytes will be locally saved, for
system reference only.

Configure S3
------------

1. Log into your console and go to the amazon s3 tool and click create
   bucket.
2. Create a user with credentials who has permissions to read/write to
   this new bucket. Also add AmazonS3FullAccess policy for the AWS user.
3. Record your Access Key ID and show your secret access key.

Enable your AWS\_S3 plugin
==========================

Edit the plugin parameters
--------------------------

Optional - Configure apache `xsendfile <https://github.com/DanielnetoDotCom/YouPHPTube/wiki/Moving-videos-directory-and-securing-files-from-direct-access-to-the-video-source-file#install-apache-xsendfile>`__
===============================================================================================================================================================================================================

    Just in case you want to hide the S3 URL

Install apache xsendfile
------------------------

::

    sudo apt-get install libapache2-mod-xsendfile && sudo a2enmod xsendfile

Configure your apache XSendFile
-------------------------------

::

    sudo nano /etc/apache2/apache2.conf

    <Directory /var/www/YouPHPTube/>
        Options Indexes FollowSymLinks
        XSendFile on
        XSendFilePath /var/www/YouPHPTube/
        AllowOverride All
        Require all granted
        Order Allow,Deny
        Allow from All
    </Directory>

``sudo service apache2 reload``

Uncomment your .htaccess file
-----------------------------

::

    sudo nano /var/www/YouPHPTube/.htaccess

    <IfModule mod_xsendfile.c>
        RewriteRule    ^videos/([A-Za-z0-9-_.]+)$ view/xsendfile.php?file=$1    [NC,L]
    </IfModule>
