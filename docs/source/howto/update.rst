Update
------

There are two ways to do it:

1 - Git Pull (Recommended)
--------------------------

go to your YouPHPTube dir and type ``git pull``

``cd /var/www/html/YouPHPTube/ && sudo git pull``

In the simplest terms, git pull does a git fetch followed by a git
merge.

You can do a git fetch at any time to update your remote-tracking
branches under refs/remotes//.

This operation never changes any of your own local branches under
refs/heads, and is safe to do without changing your working copy. I have
even heard of people running git fetch periodically in a cron job in the
background (although I wouldn't recommend doing this).

A git pull is what you would do to bring a local branch up-to-date with
its remote version, while also updating your other remote-tracking
branches.

`Git Documentation <https://git-scm.com/docs/git-pull>`__

Problems:
~~~~~~~~~

Some users some times change a file, and can not do a git pull command,
usually they get this error:

    ... Please, commit your changes or stash them before you can merge.
    Aborting


    
the solution is to force to overwrite your files, you can do this
command.

``git fetch --all && git reset --hard origin/master``

Check this video to know how to do it:
https://tutorials.youphptube.com/video/force-git-to-overwrite-files

2 - Download and Upload files
-----------------------------

Use your favorite file transfer to download a `master copy of
YouPHPTube <https://github.com/DanielnetoDotCom/YouPHPTube/archive/master.zip>`__
and upload it to your site.

Unzip it and replace all files in your YouPHPTube-root. Do not clear or replace the **videos**-folder.


Always - Database-update!
-------------------------

Remember, always check your **YouPHPTube menu -> Update version** to run
a script update. **Never skip a version!**
