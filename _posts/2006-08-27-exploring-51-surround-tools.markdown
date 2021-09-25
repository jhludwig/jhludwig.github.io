---
title: "Exploring 5.1 surround tools"
date: "2006-08-27"
tags: 
  - "halloween"
  - "sfx"
---

I'm working on creating some surround sound effects for my halloween setup this year. I've been looking for software to do this cheaply but no such luck so far.

I am starting with regular stereo flac files from various sfx discs i've purchased over the years. I'm using the 5.1 panning features of [Sony Acid Pro](http://www.sonymediasoftware.com/Products/ShowProduct.asp?PID=1005&KeyCode=7777-4701) to create a static path for the sound thru my listening space -- this is pretty easy once you understand the complexities of Acid Pro. This leaves with an AcidPro-proprietary format ffile which you can play with AcidPro. For my purposes this might be good enough.

However it would be nice to create AC3 files that could be played on arbitrary PCs, burnt to dvd, etc. AcidPro will render AC3 files but it is another $199 for the codec pak to do this. I haven't found much on the web for a free way to render AC3 -- one thought tho is to loop back the spdif output from the pc to another soundcard and capture the incoming spdif stream -- [this post suggests how to do that](http://forum.doom9.org/showthread.php?s=&postid=338286). But this is not going to be cheaper than just buying the codec pak.

I'd like to find some filter that could capture the spdif stream before it leaves the pc.

Another issue is playback. I am using winamp for playback (because i am playing with the [discolitez](http://discolitez.com/) plugin) and winamp doesn't natively support ac3 playback. [WinAmpAC3](http://www.free-codecs.com/download/WinampAC3.htm) looks like it may do the trick tho.
