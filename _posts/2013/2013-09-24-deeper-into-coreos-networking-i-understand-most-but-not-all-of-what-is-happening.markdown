---
title: "Deeper into CoreOS networking -- I understand most but not all of what is happening"
date: "2013-09-24"
---

OK so I brought up a CoreOS instance using Vagrant/virtualbox on my machine. I am trying to understand the network config and how traffic is managed and routed to the containers. From spelunking around the web, here is what I think is happening:

- CoreOS uses iptables to control routing and deliver to containers.
- By default the iptables rule set is totally open -- everything accepted, everything permitted, everything routed. ie, /sbin/iptables -L indicates that there are no rules set and the defaults are ACCEPT.
- As an option, one could create an iptable firewall config and define a systemd config file that ran it. So system-wide restrictions can be implemented.
- Additionally/alternatively, the individual containers can define iptables firewalls (using systemd or whatever in those containers).
- you have a very permissive iptables setup in coreos, you are letting all
- OK besides the inbound ethernet interface, CoreOS defines a bridge interface for the containers to use.
- Per http://blog.docker.io/2013/03/docker-containers-can-haz-networking-now/, Docker analyses the bridge definition and uses that to assign IP addresses to the containers that start up. This is how containers get their IP addresses.
- The Docker command line can also be used to map certain inbound ports to the container. Docker will twiddle the nat table rules to achieve this.

OK so this makes sense. so now let's look at what is actually happening on my system when I bring up CoreOS in a VM, with two containers, an ubuntu and a centos container.

- "/sbin/iptables -L" confirms that iptables is totally permissive. Check
- "/sbin/iptables -L -t nat" shows that Docker has indeed inserted itself into the nat table, the appropriate nat rules are there along with the necessary masquerade rule. Check.
- "/sbin/brctl show" lists two virtual ethernet connectors, one per running container. When I kill a container, one disappears. Check.
- "/bin/ifconfig" starts to confuse me a little. after the one container is killed, with only one running, i get the following interfaces:
    
    - bond0: I understand what a bonded interface is, but this seems like a rump inteface. No ethernet address, no aliasing i can find anywhere, there is nothing to bond? there is no packet traffic over the interface.
    - docker0: ok this makes sense, this is the previously defined bridge for the containers, check.
    - enp0s3: this has a reasonable looking IP address and is probably the virtual interface for the coreos host, check.
    - gre0: ok this is usually for ip tunneling, as is the next. But i am not tunneling anything I don't think? And again no traffic on it.
    - tunl0. no traffic on it.
    - lo: standard loopback, check.
    - vethXXXX: this is the adapter for the active container, check.
    - within a container, ifconfig shows me the virtual ethernet interface and a loopback interface, and iptables is wide open. check.

So I think I understand the lay of the land. Maybe the tunneling and bonding are just created for all configs but only used in certain uses?

UPDATE: the good people on the coreos google group helped me out, the bond/gre/tunl adapters are temporary artifacts that are unneeded and will go away.
