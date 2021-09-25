---
title: "Trying to get set up a Raspberry Pi dev environment on OSX"
date: "2012-09-30"
tags: 
  - "osx"
  - "raspberry-pi"
  - "software"
  - "tweet"
---

[![](images/3097197970_873351cb3e_n.jpg "http://www.flickr.com/photos/jmsmith000/")](http://theludwigs.com/wp-content/uploads/2012/09/3097197970_873351cb3e_n.jpg)I've been trying to get a Raspberry Pi dev environment set up on OSX. I'd like to have a cross compiler, a full linux build, an emulator all operational.

There is a pretty clear outline at "RPIforum from earlier this summer":http://www.rpiforum.net/forum/tutorials/article/16-a-raspberry-pi-emulated-environment-on-osx-lion/. I've had partial success:

\* Install Xcode and Xcode command line tools. No problem, I had these around anyway \* Install "homebrew":http://mxcl.github.com/homebrew/. A package manager for OSX, a good thing to have. Installing this is what finally "broke my existing flawed OSX install":http://theludwigs.com/2012/09/beware-the-osx-migration-assistant/ and drove me to reinstall OSX. But installed super cleanly once I had a fresh OSX \* Install the dependencies for ARM toolchain: brew install mpfr gmp libmpc libelf texinfo. There is a known error with mpfr compilation, so reinstall that with flags "per homewbrew wiki":https://github.com/mxcl/homebrew/issues/15061. \* Then install the Arm tools. BTW, you can't just copy and past the script from the RPI forum page because of the damn smart quotes -- echo “export PATH=$HOME/rpi/arm-cs-tools/bin:$PATH” » ~/.bash\_profile will utterly fail \* Then compile kernel. This step is unfortunately failing late in the process, I think at the linking stage. Still digging into. I have tried an alternative recipe at "the elinux site":elinux.org/RPi\_Kernel\_Compilation, it fails as well, in both cases unhappy with the vmlinux file. \* Then install the qemu emulator. the rpi forum recipe is missing a dash, should be a double dash in front of the use-gcc flag i believe. works fine with that change

So I feel close. Just need to dig into the kernel compile problem. Here are the details, I need to study the make file to figure out exactly where this occurs:

``

==> make ARCH=arm CROSS_COMPILE=~/rpi/arm-cs-tools/bin/arm-none-eabi- -k > compile.txt size: file: arch/arm/boot/compressed/../../../../vmlinux is not an object file size: file: arch/arm/boot/compressed/../../../../vmlinux is not an object file size: file: arch/arm/boot/compressed/../../../../vmlinux is not an object file size: file: arch/arm/boot/compressed/../../../../vmlinux is not an object file arch/arm/boot/compressed/vmlinux.lds:77: undefined symbol `__OBJC' referenced in expression make[2]: *** [arch/arm/boot/compressed/vmlinux] Error 1 make[1]: *** [arch/arm/boot/compressed/vmlinux] Error 2 make[1]: Target `arch/arm/boot/zImage' not remade because of errors. make: *** [zImage] Error 2 make: Target `_all' not remade because of errors.``
