You are getting this error:

**Unable to extract Initial JS player signature function name**
...because youtube-dl is not up-to-date. Google has been changing the way to access YouTube videos more frequently now than was the case a few years ago, so in order to keep youtube-dl up-to-date, it has to be updated more frequently too. To install the latest version of youtube-dl open the terminal and type:

`sudo apt-get install python-pip`

`sudo pip install youtube-dl`

To upgrade youtube-dl to the latest version:

`sudo pip install --upgrade youtube-dl`

It's crazy how frequently Google has been changing the code for accessing videos on YouTube. I seem to have remembered updating youtube-dl only a couple of month's ago, but it still couldn't download the selected video until I updated it.

We got this from: https://askubuntu.com/questions/598200/youdtube-dl-failed-to-extract-signature