---
title: "I've been stuck in linux startup morass this week"
date: "2013-09-05"
tags: 
  - "boot"
  - "linux"
---

Kickstart and Anaconda. Grub. Syslinux/isolinux. UEFI boot vs BIOS boot. USB key boot vs ISO image boot. Secure boot. Virtual Machine boot vs physicalized boot. Building packages. Integration with Puppet/Chef/Ansible/Salt. What a mess of configuration parameters, configuration files and syntaxes, constrained execution environments, etc. Design piled on top of design on top of design. Clearly the entire hairball should be reconsidered.

The most annoying impediment to deal with was the btusb bluetooth driver that singlehandedly would prevent the entire system from booting. Struggling to understand the design decisions that led to a system that can be taken down by a stupid race condition with the bluetooth driver. Bluetooth, for gosh sake.
