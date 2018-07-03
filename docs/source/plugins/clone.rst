The clone-plugin
^^^^^^^^^^^^^^^^

This Plugin helps you to clone YouPHPTube sites, it is really helpful
for backup routines, load balance, etc.

Check our video tutorial:
https://tutorials.youphptube.com/video/backup-or-clone-your-site

The Feature
===========

In this Feature we have two ends. clients (The Clone) and server (The
Master).

Important to inform that every time it is cloned the **Client** database
will be overwritten with the **Server** database, so if you have upload,
comment or view any video on the client, it will be lost.

The Process
===========

Basically the process is like that ...

1. The Client ask to the Server permission to clone him
2. The Server Accept the permission
3. The Server makes a Dump of his database, and creates a list of its
   videos and images (With the file size and Modification time)
4. The Client download the database file from the Server and overwrite
   his own database with the downloaded one
5. The Client compare the videos and files list with his own video and
   files and download the new and the modified files.
6. The Client notify the Server the Job and the server delete the
   generated dump file

Configuration
=============

-  **You will need two YouPHPTube installations (Client and Server),
   with the latest commit on both.**
-  **You must enable the CloneSite Plugin on the Client and on the
   Server**

Client
------

The Client is a YouPHPTube Site Clone

Follow those steps on your Client

1. Fill the **cloneSiteURL** parameter with the server site
2. Click on the Green Button **"Clone Now"**
3. You may be notified with *"The URL ... was just added in our server,
   ask the Server Manager to approve this URL on plugins->Clone
   Site->Clones Manager (The Blue Button) and Activate your client"*. So
   that means your need to approve your client on the Server, otherwise,
   the clone process will start

Server
------

The Server is also a YouPHPTube Site where the clients will be cloned
from

To approve clients to clone your site click on the blue button **"Clones
Manager"** and the on the green button **"Activate"** on the left side
of the client you want to approve.
