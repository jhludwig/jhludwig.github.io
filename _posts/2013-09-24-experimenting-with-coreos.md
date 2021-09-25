---
title: "Experimenting with CoreOS"
date: "2013-09-24"
tags: 
  - "appliance"
  - "linux"
---

[CoreOS](http://www.coreos.com) seems like a very nice idea -- a minimal linux kernel with just enough libs to run and manage containers. So a container-ready linux kernel, systemd to launch and maintain containers, and etcd to communicate settings (key-value pairs) across containers. The project is motivated by high scale datacenter needs, but i think it is a much more general idea, i see applications in the appliance space as well -- managing the software load on a widely deployed set of appliances is hard for many of the same reasons that managing the software load in a datacenter is hard.

I have been using a Centos kernel for my appliance experiments but am going to try a quick coreos experiment. There are some things I don't understand yet -- coreos at this point is focused on virtualized environments and the bare-metal support is just coming along. SystemD is cool but if the containers are centos based, not quite sure how that is going to work out. and networking within the appliance is confusing to me, the coreos docs suggest that one of the containers can manage all the traffic distribution but i am not quite clear on how that works at all levels -- dhcp, dns, iptables, nginx, etc etc etc.

So lots to learn! Digging in...
