---
title: "Connecting to Time Capsule from Windows"
date: "2008-03-22"
tags: 
  - "software"
  - "time-capsule"
  - "windows"
---

My time capsule was easy to setup to back up my macbook but I also wanted to use it a file share for my windows PCs. It was not obvious at all how to connect to it from Windows. The Time Capsule doesn't show up in any of the network browsing UI. I finally downloaded the Airport utility for Windows and installed it, this let me look at the Time Capsule properties and I observed the default name of the Time Capsule -- "John Ludwig's Time Capsule" -- is converted to a usable network name -- "John-Ludwigs-Time-Capsule.local". I was able to connect to this name in the Windows Explorer and map a drive to it and now all is well. There are also options in the Airbook utility to set the Workgroup for the time capsule and the WINS server, but in a home network, who knows where the freaking WINS server is??? I sure don't.
