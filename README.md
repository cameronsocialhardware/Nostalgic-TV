Nostalgic-TV
---
<h4>Use the Raspberry Pi to autoplay public domain TV shows and films for dementia sufferers</h4>
Forked from roiyz/PiVidBox

<h3>Overview</h3>
A simple way to autoplay curated lists of public domain TV shows for those suffering from dementia.
Live-streaming services can be difficult for people with dementia to operate and potentially sensitive content can appear unexpectedly on live television channels leading to unnecessary distress. The aim of this project is to create an open-source media system that utilises curated public domain content to provide a safe and enjoyable viewing experience for dementia suffers. 

<h3>Hardware</h3>
Here is the list of items required for this project:</br></br>

+ Raspberry Pi
+ USB Stick
+ USB A-Male to A-Female extension cord
+ HDMI cable

<h3>Instructions</h3>

The run.sh file should be placed under the /home/pi directory.

You should also modify its attributes to be an executable file by using the following command:

`chown +x /home/pi/run.sh`

When executed, the script tries to enumerate all video files on the USB drive ending with .avi or .mp4, then shuffles them, and asks OMXplayer to play it one by one. When the cycle ends, the script sleeps for a bit, and then tries to start the play cycle again.

Once you have the script copied, prepare a USB drive with .mp4 public domain television shows in the root folder and plug it into your Raspberry Pi.

Next, run...

`sudo echo "/home/pi/run.sh" | sudo tee /etc/xdg/lxsession/LXDE-pi/autostart`

Then run...

`sudo reboot`

Once your Raspberry Pi has rebooted, you're ready to start using your Nostalgic TV!

