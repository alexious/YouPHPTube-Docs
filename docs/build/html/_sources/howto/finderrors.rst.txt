In order to effectively manage YouPHPTube, it is necessary to get
feedback about the activity and performance of the server as well as any
problems that may be occurring.

YouPHPTube stores error and activities logs in
``/your/path/to/YouPHPTube/video/youphptube.log``

To monitor the responses and activities of the YouPHPTube service I use
the following command:
``tail -n 200 -f /var/www/YouPHPTube/videos/youphptube.log``

Sometimes it is also necessary to check the logs of your operating
system, such as apache error, apache log, mail log, etc.

Also you can try to find errors on JavaScript or Ajax Request
https://github.com/DanielnetoDotCom/YouPHPTube/wiki/Check-Ajax-answer
