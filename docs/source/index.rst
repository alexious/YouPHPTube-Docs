Welcome to YouPHPTube's doc
^^^^^^^^^^^^^^^^^^^^^^^^^^^

You just find a open video-plattform.

This project has a huge functionality and can be used for various scenarios.

For example, we provide:

- A streamer, for watching the videos
    - Various filetypes
        - Local MP4 and Audio
        - linked MP4 and Audio
        - Live-streams
        - Torrent MP4 (in development)
        - AWS S3-compatible Storage (commercial plugin)
        
    - Various plugins
        - A lot of plugins allow you to customize
            - Your player
            - Your main-view / template
            - Your logins (Google, Facebook...)
            - Your server-load
            - Your video-storage
    
    - Tracking the watched videos by views
    - Use channels and subscriptions
            
- A encoder
    - Allow you to upload almost any format on another server and save it local on your streamer
    - Direct youtube-download-support
    

For more information, read our `Readme <readme.html>`__

Installation
^^^^^^^^^^^^

This is a project that is developed by us. Like for every other php-script, it's good to collect some admin-expiriences, so you can handle your system.

If problems appear, consider read the troubeshoot-guide downer. In case it does not solve it, follow the guide to do a proper issue at github.

Our code support various systems and we have some howto's to setup a entire server as well. Mainly, we support and test Apache and Ubuntu (and Nginx for live-streamer-setup). 

If you choose other systems, you propaply need to know them and maybe some general . If you like to provide a howto, this is welcome!

-  `Install YouPHPTube-streamer and encoder on Ubuntu 16 <install/installUbuntu16.html>`__
-  `Install YouPHPTube-streamer and encoder on Ubuntu 18 <install/installUbuntu18.html>`__
-  `Install YouPHPTube-streamer and encoder on Debian 9.3 <install/installDebian93.html>`__
-  `Setup live-stream (video-tutorial) <https://tutorials.youphptube.com/video/10-min-youphptube-stream-server-installation>`__
-  `Nginx-support for  YouPHPTube-streamer and encoder <install/nginx.html>`__
-  `MS IIS-support for YouPHPTube-streamer <install/iis.html>`__

Configuration
^^^^^^^^^^^^^

-  `How to update your YouPHPTube <howto/update.html>`__
-  `Howto Install a new Plugin <howto/installplugin.html>`__
-  `Automatic Thumbs (JPG-GIF) on direct uploaded MP4
   videos <Automatic-Thumbs-(JPG-GIF)-on-direct-uploaded-MP4-videos>`__
-  `Setting up YouPHPTube to send
   emails <Setting-up-YouPHPTube-to-send-emails>`__
-  `Redirect http to https <Redirect-http-to-https>`__

Plugins
^^^^^^^

- `Advanced Customization Plugin <plugins/advancedcust.html>`__
- `AWS S3 on YouPHPTube <plugins/aws.html>`__
- `Configure LDAP-Plugin <plugins/ldap.html>`__
- `Cache-Plugin <plugins/cache.html>`__.


Paid plugins, support and development
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

We have some advanced functionality in form of plugins, we sell. Please
have a look at https://easytube.club .

Some examples:

- Change resolutions 
- Subtitles 
- Secure videos folder 
- VR360-Video 
- Livesearch 
- and many more...

Performance
^^^^^^^^^^^

When you have a lot of users, your server can reach it's limits. To
prevent this, there are some things possible. 

- Use a host with mysqlnd enabled! We provide support for non-mysqlnd-host's, but we have a SQL-cache for mysqlnd only. Also, this is a fast, native driver (better performance anyway). If you are unshure if you have this, ask your hoster. 
- Enable minify of javascript! This helps only, to reduce the bandwidth a little. Go to advanced customization-plugin and enable "Minify JS". Clear videos/cache after this! 
- Enable the `Cache-Plugin <Cache-Plugin>`__ 
- Disable gifs(Gallery- and Youphpflix-plugin) or not set gifs (use less bandwidth)

Livestream
^^^^^^^^^^

-  `Setup streamer (video-tutorial) <https://tutorials.youphptube.com/video/10-min-youphptube-stream-server-installation>`__
-  `Record Live Stream <Record-Live-Stream>`__
-  `Configure NGINX Stream Resolutions <Configure-NGINX-Stream-Resolutions>`__

Troubleshooting
^^^^^^^^^^^^^^^

Various things can cause problems. Here, you find steps that eventualy
fix your problem. If it doesn't, please read `Check Ajax
answer <Check-Ajax-answer>`__ and `How to find errors on
YouPHPTube <howto/finderrors.html>`__ for a usefull issue -
this makes it easier for us to help you.

-  Recheck, if all database-upgrades are done (**Menu -> Update version**)
-  Clear the cache-folder (delete all files in **videos/cache/**)
-  Ad-managment is broken? Try disable your adblocker
-  `How to find errors on YouPHPTube <howto/finderrors.html>`__
-  `Check Ajax answer <Check-Ajax-answer>`__
-  `Mysql Troubleshooting <Mysql-Troubleshooting>`__
-  `Message when rewrite is not set / 404-Errors / install rewrite-modules <Message-when-rewrite-is-not-set>`__
-  `Error while sending QUERY packet cpanel <Error-while-sending-QUERY-packet-cpanel>`__
-  `Encoder-Errors <trouble/encodertroubles.html>`__

Known problems
^^^^^^^^^^^^^^

-  If the chart is not counting videos, try disable the `Cache-Plugin <plugins/cache.html>`__.
