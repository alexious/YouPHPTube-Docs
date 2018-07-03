Plugins are utilities which provide additional functionality to your
YouPHPTube. To install a plugin you just need to put the plugin zip
file. Once a plugin is installed, you may activate it or deactivate it
from the Plugins menu in your plugin manager.

To install a plugin you have two options:

1 - Use the app plugin button
-----------------------------

To use this button, make sure you have the unzip app on your server

``sudo apt-get install unzip``

You will also need to make the plugin dir writable before upload

``chown www-data:www-data /var/www/html/YouPHPTube/plugin/ && chmod 755 /var/www/html/YouPHPTube/plugin/``

If you still not sure ho to do it, take a look on this video:
https://tutorials.youphptube.com/video/donwloading-and-installing-a-plugin

2 - Upload the unziped Folder
-----------------------------

Unzip the file and upload this to the plugin directory on your
YouPHPTube server. Usually the directory is
``/var/www/html/YouPHPTube/plugin/``.

The Folder must be the same name as the file inside, for example, if you
are uploading the *Video Resolution Switcher plugin*, you should have a
directory name called

::

    VideoResolutionSwitcher 
       |_ VideoResolutionSwitcher.php
       |_ Other files ...
