This Plugin was designed to help your video site, handle huge traffic.
----------------------------------------------------------------------

The way this plugin is right now, it improves the page build speed at
least in 100x better

Options
~~~~~~~

**enableCachePerUser = false;**

each user will have his own cache, it reduces the cache performance

**enableCacheForLoggedUsers = false;**

usually when a user is logged the cache is disable, because is common to
have dynamic content on it (comments, likes, etc)

**cacheTimeInSeconds = 600;**

Cache life time

**cacheDir = 'videos/cache/';**

Where to save it

**logPageLoadTime = false;**

Write each page load time on log file, it is good to check the results

Know Problems
~~~~~~~~~~~~~

Embed videos count
^^^^^^^^^^^^^^^^^^

Your embed videos count will not count a new view until cache expire.
#### Change layout button you will not be able to change layout, because
the cache is based on the URL, you will not be able to have 2 different
layouts on the same URL
