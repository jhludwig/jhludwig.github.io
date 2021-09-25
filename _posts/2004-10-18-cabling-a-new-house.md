---
title: "Cabling a new house"
date: "2004-10-18"
tags: 
  - "tech"
---

So my dad is building a house and wants some advice on cabling -- what should he run, what topology. He is building from scratch, all the walls will be open, so he can do whatever he wants.

So based on my experience and the wise counsel of [sam](http://www.mckelvie.org) and [rich](http://www.rongfamily.com), here is what I'd do dad.

\* **establish a wiring closet** in your basement. All your exterior lines will enter here -- phone, cable, satellite, etc. \* run all cabling in a **star topology** from this closet. \* as a basic cable pack, try to use **standard ?structured cable?** -- cat5e + 2 coax, can be purchased in a single bundled cable (http://www.cablestogo.com/product.asp?cat%5Fid=314&sku=43075) which makes install easier. With this setup you can handle 4 phone lines, gbit enet, and two video feeds (for say dual tuner tivo boxes) \* do not let anyone talk you into cat5 instead of **cat5e** \* make sure the coax and all coax connectors/splitters are **HDTV friendly** -- ie 1ghz parts, not the old 900mhz parts. I had to replace a bunch of splitters on my patch panel this year to allow for HDTV signals, you don't want to do this. \* if you have extreme video needs you may want to run additional rg6 (coax) cables to your home theater setup. Sam explains: _currently, four RG6 cables are required to support unlimited DSB devices (four cables come out of the satellite dish; these are multiplexed onto a single cable for each tuner). That number could increase as the number of LNB's increase (currently 3 for HD DirecTV). I recommend running at least 4 RG6 cables to each location that will potentially host a multi-tuner receiver (e.g., Tivo)._ \* run your standard cable pack to any spot you have a tv or phone -- family room, den, kitchen, bedrooms, basement, garage. For rooms that may see a lot of use -- family room, office -- run two or three sets. \* and I'd run an extra set of cables and leave them unused in the attic or crawlspace for the family room and office. When you remodel later and want cables in a different place, you can easily pull the unused set down.

**What about wireless lan and wireless phones?** Well I have a whole pile of discarded wifi and wireless phone gear at my house. I personally am unsatisfied with coverage, quality, and security/complexity. I'd reserve wireless use for particular rooms -- you can always put a mini wifi access point in a room for wifi in that room if you need it at some point. But as long as your walls are open, I'd run the cabling.

**What about multiroom audio?** I don't think running special analog cables is worth it, the scenarios that this supports are pretty limited. You can always slap a small pc or remote media player box like the [squeezebox](http://www.slimp3.com/) in additional rooms if you want access to your music collection in these rooms.

**What about intelligent lighting?** Well I don't have it and haven't missed it. Sam has some more sage advice if you want to go down this path: _If home automation is of interest, I'd consider adding a control line to each switch box (cat5, for example). At a minimum, make sure power, neutral, and ground are available at every switch box (light switch-boxes sometimes are missing neutral or ground), so that powered components can be added at the box._
