---
title: "I'm kind of in container/vm hell right now, I must be doing it wrong."
date: "2013-09-26"
---

[![www.CGPGrey.com](images/russiandolls-300x199.jpg)](http://theludwigs.com/wp-content/uploads/2013/09/russiandolls.jpg)So I have a Docker/Ubuntu VM running in virtualbox via vagrant, and am building new docker images that i can use as containers in another virtualbox vm running coreos, and i need to copy files around between all these, and ssh between them, and manage all the variants of images that each of these needs, and manage packages across all these (and trying to avoid using different package managers between all these), and oh yes i also spin up vms at a cloud service and need to shuttle things up there and back, and also i need to build some physical install images for real hardware, and manage all the images and packages for that, and jeepers this is all confusing as hell. so many levels of containment and slightly different containers and key management and network management and i just want to blow my brains out at some point.

Feels like there is a need for a new type of IDE that manages all this crap and keeps it straight for you. A container/cloud focused IDE. The emergent wave of cloud IDEs are great for the cloud but they don't really help me with all this other stuff.

Maybe I am doing it wrong? Maybe I should just dump virtualbox (which is kind of a buggy mess anyway) and just shift everything to cloud vms on a particular cloud service? that has some appeal, but i am thinking about building appliances and ultimately i need code running right here in boxes here, accessing real devices and inputs here.
