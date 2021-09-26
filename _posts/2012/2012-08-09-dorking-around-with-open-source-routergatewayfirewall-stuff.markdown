---
title: "Dorking around with open source router/gateway/firewall stuff"
date: "2012-08-09"
tags: 
  - "firewall"
  - "network"
  - "opensource"
  - "router"
  - "tweet"
---

[![](images/6855809752_35cd52feff_n.jpg "http://www.flickr.com/photos/hades2k/")](http://theludwigs.com/wp-content/uploads/2012/08/6855809752_35cd52feff_n.jpg)Just for yucks I am using a linux box in my house as gateway for all the devices in my house, I just want to be able to see what is going on at the network level and do a little more finegrained control.

I considered using "dd-wrt":http://www.dd-wrt.com/site/index but it is not keeping up with router releases -- it is not available for any of the routers on the shelf at best buy locally, for instance. and these router boxes are kind of a mess anyway, super limited on ram and storage, which constrains what I can do. i can easily build a cheap linux box with ethernet in, wifi out. the only advantage the router boxes have are the 4+ onboard wired ethernet ports. but wired ethernet seems to be going the way of the dodo in the home.

There are a ton of code bases to choose from. Here are some that seemed notable

\* "untangle":http://www.untangle.com/. commercial product but also some open source light version which they try to hide on their site. which makes me think the open source thing is 99% of the commercial thing. nice UI. They obviously don't really want to support people like me tho, probably will steer away from this. \* "clearOS":http://www.clearfoundation.com/Software/overview.html. similar but looks even more open-sourcy, they say the right things about supporting open source community. \* "ipfire":http://www.ipfire.org/. very open sourcy and modern (git repositories for instance). git repositories seem active \* "zeroshell":http://www.zeroshell.net/eng/. old school open source (not git based for instance), looks a little rough around the edges, but very complete. \* "devil linux":http://www.devil-linux.org/home/index.php. boots off cd/usb so easy to try but doesn't seem to have the network depth of the previous choices

i'll probably start with an ipfire trial. unless someone has a better idea.
