Nginx
^^^^^

Nginx is only experimental supported for the moment.

Since we have php-routing enable, this should be possible:

https://github.com/skipperbent/simple-php-router#setting-up-nginx

Thanks to patriclougheed, there are also two config-files for nginx
(this solution surround the php-router above):

-  `Streamer <https://gist.github.com/patriclougheed/706677ffe2459df3b6587e54fd4a0923>`__
-  `Encoder <https://gist.github.com/patriclougheed/29a6d997a1371952e29bd8384ea9bf4e>`__
   (this is needed anyway, until php-router also reaches the encoder)

Both methods should work. You can find it's issue here:
https://github.com/DanielnetoDotCom/YouPHPTube/issues/691