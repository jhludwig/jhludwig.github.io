---
title: "It&#039;s a Google Google Google Google World"
date: "2004-10-17"
tags: 
  - "tech"
---

\* Both [Paul Thurrott](http://www.internet-nexus.com/2004_10_03_archive.htm#109715484125476438) and [Gadgetopia](http://www.gadgetopia.com/2004/10/09/GMailFSForWindows.html) point towards the [Gmail shell extension for Windows](http://www.viksoe.dk/code/gmail.htm) \* Via [engadget](http://www.engadget.com/entry/2511742306349375/), Google SMS launches \* Of course, the [Google desktop launched](http://desktop.google.com) and [Jon Udell has found ways to let it search firefox history](http://weblog.infoworld.com/udell/2004/10/15.html#a1096)

Like the rest of the planet I installed the Google Desktop over the weekend. No noticeable perf drag on my system.

I had read that it would not work against network drives, but I have ?My Documents? folder pointed to a network drive and indexing worked fine, [ben](http://www.slivka.com) pointed this nice fact out to me. I'd like it to pick up some other network shares and I wonder if it can be coerced into doing so -- I don't see any ini file, the only likely seeming reg key is an empty key named CRAWL\_DIRS, I wonder what it does?

As [rich](http://www.tongfamily.com) and ben and I discussed in email, we all noted the contrasts between the google desktop and winfs (and its intellectual precursor, ofs in cairo). Hmmm, there may be some architectural and project management lessons to be learned here. A light layer on existing storage both works and is shipping. Further benefits will accrue as developers and users provide fb, allowing google to incrementally improve and expand the facility -- while winfs is still not shipping.
