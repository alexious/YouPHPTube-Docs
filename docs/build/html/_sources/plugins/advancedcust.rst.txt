What is this
============

The intent of this plugin is to allow the site administrator to
fine-tune both the streamer and the encoder.

Options
=======

$obj->doNotShowUploadMP4Button = false;
---------------------------------------

If you set it to true users will not be able to see the "Upload a MP4
video" button

$obj->doNotShowEncoderButton = false;
-------------------------------------

If you set it to true users will not be able to see the "Encode video
and audio" button

$obj->doNotShowEmbedButton = false;
-----------------------------------

If you set it to true users will not be able to see the "Embed a video
link" button

$obj->doNotShowEncoderResolutionLow = false;
--------------------------------------------

If you set it to true users will not be able to see the option on
encoder to convert videos to **Low Resolution**

$obj->doNotShowEncoderResolutionSD = false;
-------------------------------------------

If you set it to true users will not be able to see the option on
encoder to convert videos to **SD Resolution**

$obj->doNotShowEncoderResolutionHD = false;
-------------------------------------------

If you set it to true users will not be able to see the option on
encoder to convert videos to **HD Resolution**

$obj->disableNativeSignUp = false;
----------------------------------

If you set it to true you will disable native sign up system, you will
need an OAuth2 authentication method, like Facebook, Google, etc

$obj->disableNativeSignIn = false;
----------------------------------

If you set it to true users will disable native sign in system. be
careful **you must make one of your OAuth users as an Admin**, otherwise
you will not be able to login as Admin anymore, unless you direct change
the database parameters
