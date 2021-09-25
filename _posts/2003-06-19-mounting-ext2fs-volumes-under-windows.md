---
title: "Mounting Ext2FS volumes under Windows"
date: "2003-06-19"
tags: 
  - "tech"
---

My cheapo [connectstor NAS box](http://www.theludwigs.com/archives/000572.html) died recently. Just started whirring and whirring, unresponsive to any remote CIFS or HTTP request. I tore it apart and mounted one of the raided 120G drives in a USB2.0 drive enclosure and started looking at it directly from my desktop machine.

First I tried [PartitionMagic](http://www.powerquest.com/partitionmagic/) on it. Good news -- the volume was recognizable. So-so news -- it was an ext2 format volume, the connectstor box runs linux of course. PartitionMagic couldn't seem to do much with ext2 volumes, I wanted to get the data off the disk.

Google suggests [Paragon Software's Ext2FS](http://www.ext2fs.com/) driver for windows. For $30 seemed worth trying, but their ecommerce site, hosted in europe somewhere, couldn't seem to take my MasterCard. probably some little trivial problem but I didn't have the patience to figure out.

Next I tried [Explore2fs](http://uranus.it.swin.edu.au/~jn/linux/explore2fs.htm "Explore2fs HomePage"). Very nice windows utility, and I could see all my files, hurray! But trying to copy them out to my windows desktop hung the app. Some of the files made it but not all.

Next I found the [Ext2fs](http://e2fsprogs.sourceforge.net/ext2.html) project on sourceforge. A real live ext2 fsd for windows. Easily installed but pretty cryptic mount instructions. I had to know the disk id and volume id i was trying to mount, and i had a little trouble discovering them. But back to Explore2fs, it told me the disk and volume id, and then i could mount using Ext2Fs.

I am now happily copying all the files over.
