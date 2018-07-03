Welcome to youphptube's doc
^^^^^^^^^^^^^^^^^^^^^^^^^^^

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

We support various systems and have some howto's to setup a entire server as well.

-  `How to install LAMP, FFMPEG and Git on a fresh Ubuntu 16.x For
   YouPHPTube version 4.x or
   newer <install/installUbuntu16.html>`__
-  `How to install LAMP, FFMPEG and Git on a fresh Ubuntu 18.x for
   YouPHPTube version 4.x or
   newer <install/installUbuntu18.html>`__
-  `Install YouPHPTube in Debian
   9.3 <install/installDebian93.html>`__
-  `Nginx <install/nginx.html>`__
-  `MS IIS <install/iis.html>`__

Configuration
^^^^^^^^^^^^^

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


Paid plugins
^^^^^^^^^^^^

We have some advanced functionality in form of plugins, we sell. Please
have a look at https://easytube.club .

Some examples: 
- Change resolutions 
- Subtitles 
- Secure videos folder 
- VR360-Video 
- Livesearch 
- and many more...

Update youphptube
^^^^^^^^^^^^^^^^^

-  `How to update your YouPHPTube <How-to-Update-your-YouPHPTube>`__

Performance
^^^^^^^^^^^

When you have a lot of users, your server can reach it's limits. To
prevent this, there are some things possible. 

- Use a host with mysqlnd enabled! We provide support for non-mysqlnd-host's, but we have a SQL-cache for mysqlnd only. Also, this is a fast, native driver (better performance anyway). If you are unshure if you have this, ask your hoster. 

- Enable minify of javascript! This helps only, to reduce the bandwidth a little. Go to advanced customization-plugin and enable
"Minify JS". Clear videos/cache after this! 
- Enable the `Cache-Plugin <Cache-Plugin>`__ 
- Disable (Gallery- and Youphpflix-plugin) and not set gifs (use less bandwidth)

Livestream
^^^^^^^^^^

-  `Setup streamer
   (video-tutorial) <https://tutorials.youphptube.com/video/10-min-youphptube-stream-server-installation>`__
-  `Record Live Stream <Record-Live-Stream>`__
-  `Configure NGINX Stream
   Resolutions <Configure-NGINX-Stream-Resolutions>`__

Various
^^^^^^^

-  `Howto Install a new Plugin <How-To-Install-a-new-Plugin>`__
-  .. rubric:: Troubleshooting
      :name: troubleshooting

Various things can cause problems. Here, you find steps that eventualy
fix your problem. If it doesn't, please read `Check Ajax
answer <Check-Ajax-answer>`__ and `How to find errors on
YouPHPTube <How-to-find-errors-on-YouPHPTube>`__ for a usefull issue -
this makes it easier for us to help you.

-  Recheck, if all database-upgrades are done (**Menu -> Update
   version**)
-  Clear the cache-folder (delete all files in **videos/cache/**)
-  Ad-managment is broken? Try disable your adblocker
-  `How to find errors on
   YouPHPTube <How-to-find-errors-on-YouPHPTube>`__
-  `Check Ajax answer <Check-Ajax-answer>`__
-  `Mysql Troubleshooting <Mysql-Troubleshooting>`__
-  `Message when rewrite is not set / 404-Errors / install
   rewrite-modules <Message-when-rewrite-is-not-set>`__
-  `Error while sending QUERY packet
   cpanel <Error-while-sending-QUERY-packet-cpanel>`__
-  `How To Install a new Plugin <How-To-Install-a-new-Plugin>`__
-  `youdtube dl failed to extract
   signature <youdtube-dl-failed-to-extract-signature>`__
-  `Encoder-Error We could not found your
   streamer-site! <Encoder-Error-We-could-not-found-your-streamer-site!>`__

Known problems
^^^^^^^^^^^^^^

-  If the chart is not counting videos, try disable the
   `Cache-Plugin <Cache-Plugin>`__.
