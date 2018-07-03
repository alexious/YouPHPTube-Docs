We create this plugin based on VMAP and VAST standards

VMAP (Video Multiple Ad Playlist)
---------------------------------

VMAP describes when an ad should be played.

VAST (Video Ad Serving Template)
--------------------------------

VAST is a Video Ad Serving Template for structuring ad tags that serve
ads to video players. Using an XML schema, VAST transfers important
metadata about an ad from the ad server to a video player.

Why These Standards Are Important
---------------------------------

It is all about scalability. In order for publishers to serve ads across
multiple platforms / devices with the video player of their choice, a
common ground to build against is required.

How to Use the plugin.
======================

To access the plugin configuration screen you can click on the red
**Advertising Manager** button on the top of the videos manager or on
the Plugin button on the right side of the AD\_Server plugin on the
plugin manager

To have your ad videos playing will need to do two things 1. Create a
campaign 1. Add videos on your campaign

Create a campaign
~~~~~~~~~~~~~~~~~

Fill all the fields on the lest side and click on the Save button The
**Max Prints** field when the ad reaches the number of views will no
longer compete with the display ads queue

Campaign List
~~~~~~~~~~~~~

On the right side you can see a list of the campaigns and buttons to add
videos, see a simple chart about the campaign progress, edit a campaign
and delete the campaign respectively.

Add videos
~~~~~~~~~~

On the first field type a name of a video, and a list will pop up below,
choose a video and fill the other fields and click on the green add
Video button

the videos choosed here will randomly appear in your campaign

Plugin Parameters
-----------------

Video Positions
~~~~~~~~~~~~~~~

-  start = Check it if an Advertising should appear on the start video
   position;
-  mid25Percent = Check it if an Advertising should appear when the
   video position reaches 25% of the full video length;
-  mid50Percent = Check it if an Advertising should appear when the
   video position reaches 50% of the full video length;
-  mid75Percent = Check it if an Advertising should appear when the
   video position reaches 75% of the full video length;
-  end = Check it if an Advertising should appear when the video
   position reaches the end of the full video length;

frequency
~~~~~~~~~

-  showAdsOnEachVideoView = This defines how often advertisements will
   appear, for example: if it is set to 2, you will see ads each 2
   videos, but if it is set to 1 you will see ads on every video;
-  showAdsOnRandomPositions = This will pick random positions to display
   the ads, but it will pic only the positions you have checked above.
   For example, if you want to have 2 random positions, but do not want
   to have videos on the start position, you must uncheck the *start*
   video position checkbox;

Others
~~~~~~

-  skipoffset = This is the percentage where the skip button should
   appear;
-  showMarkers = Check it if you want to show the yellow markers on the
   video, where the advertising should appear;
