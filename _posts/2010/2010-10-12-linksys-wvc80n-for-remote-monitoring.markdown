---
title: "Linksys WVC80N for remote monitoring"
date: "2010-10-12"
tags: 
  - "camera"
  - "network-gear"
  - "tweet"
---

Installed a Linksys WVC80N for remote monitoring of a site. Mentioned this to a few folks and they seemed excited about, apparently this is a common need.

The camera hardware itself was easy to set up and the hardware is solid. I did the setup on a Mac and had no problems getting the camera set up and working on the wireless network.

At that point, tho, you have to go offroad. Assuming you want to have remote access to the video, you have a couple paths to try out:

\* You can set up motion detection-driven email/ftp alerting. You have to use all the camera admin pages but it seems pretty straightforward. But I didn't do this. So no idea how well the motion detection work. \* Or you can set up a dynamic dns connection through TZO.COM. The camera web pages claim there is a free trial, but the TZO website did not work for the free trial. Kind of a screw job Cisco, you should do better. The cost for a year of service for TZO was not crazy tho so I just signed up for a year of service. You get a www.yournamehere.myipcamera.com domain which you can connect to from anywhere. And it does work, I am looking at my camera now. But it took a LOT of futzing with firewall rules and port mapping on my dsl modem/router to punch thru. All these devices claim they have some magic UPNP technology to help you do all this but that seems to be baloney. So be prepared to futz or have someone futz for you. \* Once it is set up, it took the TZO.COM dynamic DNS service 24 hours or so to be reliable. Probably takes that long for DNS entry to percolate around.
