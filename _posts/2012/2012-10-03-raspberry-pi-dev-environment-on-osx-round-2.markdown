---
title: "Raspberry Pi Dev Environment on OSX, round 2"
date: "2012-10-03"
tags: 
  - "raspberry-pi"
  - "tweet"
---

OK I am still "stymied by a linker problem":http://theludwigs.com/2012/09/trying-to-get-set-up-a-raspberry-pi-dev-environment-on-osx/ in getting a native OSX Raspberry Pi dev environment set up. Stymied might be a strong word, I haven't looked the make file nor have I spent any time cruising the various forums to see if there is an answer to my problem.

That is because I have moved on to another approach -- a vm-based approach. And I am successfully compiling now. The setup:

\* Install the "Virtual Box":https://www.virtualbox.org OSX software, and create a new Ubuntu VM. \* Download the latest "Ubuntu image":http://www.ubuntu.com/download \* Bring up the VM, and then follow the recipe at "elinux":http://elinux.org/RPi\_Kernel\_Compilation for a foreign Ubuntu machine. Note that these instructions assume you are transferring the image over to a raspberry pi and have a lot of extra steps. I am just trying to get to an image I can run in an emulator, and so once the kernel is compiled, I can flip over to the instructions at... \* ..."RPIForum":http://www.rpiforum.net/forum/tutorials/article/16-a-raspberry-pi-emulated-environment-on-osx-lion/. I could run the QEMU emulator inside Virtual Box at this point, but running an emulator inside a vm seems a little nutty. So at this point I can pull the zImage image out of the VM and run the native osx qemu emulator.

So still a little Rube-Goldbergian, but working and viable. And since most of the work is done in a VM, I can move the setup over to a Windows machine or a Linux machine or wherever.
