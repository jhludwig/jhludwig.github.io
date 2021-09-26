---
title: "If you are coming from the PC universe, the Raspberry Pi boot sequence is funky"
date: "2012-10-03"
tags: 
  - "pc"
  - "raspberry-pi"
  - "tweet"
---

[![](images/3687611776_a4811d0f6f_n.jpg "http://www.flickr.com/photos/warrenski/")](http://theludwigs.com/wp-content/uploads/2012/10/3687611776_a4811d0f6f_n.jpg)Read the "RPIforum":http://elinux.org/RPi\_Software outline carefully. No boot rom, no boot loader. Instead:

> The boards do not include NAND or NOR storage - everything is on the SD card, which has a FAT32 partition with GPU firmware and a kernel image, and an EXT2 partition with the rootfs. We're not currently using a bootloader - we actually boot via the GPU, which contains a proprietary RISC core (wacky architecture). The GPU mounts the SD card, loads GPU firmware and brings up display/video/3d, loads a kernel image, resets the SD card host and starts the ARM.

I was hopelessly confused as to why I needed a kernel image and a system disk image until I read this. It is no goofier than the PC BIOS but is just different.
