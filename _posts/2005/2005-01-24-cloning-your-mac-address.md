---
title: "Cloning your MAC address"
date: "2005-01-24"
tags: 
  - "digitalhome"
---

To take full advantage of the [Network Magic](http://www.purenetworks.com) beta release (i'm on the board), I decided to upgrade my router/firewall from a sonicwall box I've had for 3-4 years to a Linksys gigabit ethernet router (i'll be switching all my nics to gigabit nics as well -- $29 for the cheapest GBE nics at fry's).

The thing you must must must do -- note the mac address of your old router first, because comcast ties your service to a specific mac address. I failed to do this and spent 10 minutes trying to figure out why my net wasn't working and then noticed that my new linksys box was unable to acquire an address via dhcp. thankfully the linksys box lets you set its mac address to whatever you want, once i made this change, things were happy.

How regular humans will ever figure this out is beyond me. I guess they will call comcast. Why doesn't comcast make this easy for their customers?
