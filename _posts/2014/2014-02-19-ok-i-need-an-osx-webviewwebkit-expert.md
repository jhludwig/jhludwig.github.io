---
title: "OK I need an OSX Webview/Webkit expert..."
date: "2014-02-19"
tags: 
  - "osx"
---

So I have a little app that hosts the Webview control and doesn't do a whole lot more. I am running it on a MacBook Pro Retina display. I've enabled fullscreen display, I've set the window in the xib to be full retina 2880x1800.

But the webview seems to think it is running at 1440x790ish or so. Basically half res. As reported by NSScreen. And it is pretty clearly running at half resolution.

The same web page looks fine in Chrome, full retina resolution.

Ah interestingly, in Safari, it is also running at half resolution. Hmmm.

Nothing obvious on StackOverflow. Nothing obvious in Apple developer doc (tho I certainly probably missed something).

UPDATE: Mr. Sobeski gave me some ideas. The retina devicePixelRatio is probably involved. Apparently this creates some problems in some configs. http://stackoverflow.com/questions/4405710/uiwebview-w-html5-canvas-retina-display might be a direction to try.
