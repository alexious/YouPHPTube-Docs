It can be nice to force https by redirect all http-content to it.

This job is basicly done by the webserver itself and therefore it is a
job for the administrator, not youphptube.

We don't like to force this, because of decrease possibilitys.

**By the way: If you use https, the website-address in your
videos/configuration.php needs to begin with https:// too.**

CPanel and similiar
~~~~~~~~~~~~~~~~~~~

You can try the downer apache-.htaccess-solution first.

If this does not work, search in your hosting-menu for a option to
enable this. There are various, we can not support all - in case of
questions, ask your hoster.

Apache
~~~~~~

Apache has two possibilitys: edit the **.htaccess**-file or change the
config from apache itself.

.htaccess
^^^^^^^^^

Add those lines to the **begin** of your **.htaccess**-file, which is in
your **youphptube-folder**:

::

    RewriteEngine On
    RewriteCond %{HTTPS} !on
    RewriteRule (.*) https://%{HTTP_HOST}%{REQUEST_URI}

That's it. **If you do not find the .htaccess-file**, search for a
option like "show hidden files".

Redirect www.youphptube.com to youphptube.com
'''''''''''''''''''''''''''''''''''''''''''''

There can be failures in view, when you setup youphptube.com but use
www.youphptube.com. You will have to redirect.

If you do so, do not forget to change the url in
videos/configuration.php, in this case to "https://youphptube.com".

Add this to the begin of your .htaccess-file:

::

    RewriteEngine On
    RewriteCond %{HTTP_HOST} ^www\.youphptube\.com$ [NC]
    RewriteRule ^(.*)$ https://youphptube.com/$1 [L,R=301]

The source is in german, i did not quickfind another doing the same:
https://seo-summary.de/301-redirect/ Untested.

Tested by author.

Apaches config file
^^^^^^^^^^^^^^^^^^^

Under debian and ubuntu, you can find the config-files under
/etc/apache2/conf-enabled/ .

There, edit the config for your needs (for example: replace the url).
The example starts with http (*:80-section) and ends with the targeted
https-connection (*:443).

::

    <VirtualHost *:80>
        ServerName www.example.com
        Redirect / https://www.example.com/
    </VirtualHost>

    <VirtualHost *:443>
        ServerName www.example.com
        # ... SSL configuration goes here
    </VirtualHost>

This solution is more proper and eventualy secure but need more
expirience and edit than the .htaccess-solution.

Untested by author.

Original-source for both solutions:
https://stackoverflow.com/questions/4083221/how-to-redirect-all-http-requests-to-https

Nginx
~~~~~

This is a redirect-example for nginx. If you use nginx, some more
expirience is good anyway. The config-files are like always in /etc,
what's the exact name for nginx can depend.

::

    server {
       listen         80;
       server_name    my.domain.com;
       return         301 https://$server_name$request_uri;
    }

    server {
       listen         443 ssl;
       server_name    my.domain.com;
       # add Strict-Transport-Security to prevent man in the middle attacks
       add_header Strict-Transport-Security "max-age=31536000" always; 

       [....]
    }

This solution is untested, source:
https://serverfault.com/questions/67316/in-nginx-how-can-i-rewrite-all-http-requests-to-https-while-maintaining-sub-dom
