---
title: "Keynes, Research, IoT, Rust, Nix, Tools, Snow/Liquid -- Things I Learned This Week"
date: "2021-02-23"
---

Or maybe this should be titled "Rabbitholes I Went Down This Week."

## Basic Research

I’m reading the [The Price of Peace](https://www.goodreads.com/book/show/49644992-the-price-of-peace) right now -- the life and legacy of Keynes.  He led a far richer more fascinating life than I had realized, and the story is very topical as we spend our way thru COVID and reconsider what is an appropriate amount of national debt.  It is hard to not be enthusiastic about even more debt after reading this.

We should probably be funding a lot more basic research.  [Ashoka Rajendra](https://ashoka.substack.com/people/1146202-ashoka-rajendra) provides a [nice explanation of how the biopharma industry developed COVID vaccines so quickly](https://ashoka.substack.com/p/an-ode-to-basic-research), how vital the whole chain of basic research and development was, and how vital the public/private partnership was.  Public-supported basic research is a hard thing to sell, but it is probably one of the most leveraged things we can do.  

Our space programs are amazing, inspiring.  Huge thanks to everyone involved for lifting us above our every day existences.  The scope at which space programs operate is hard to fathom — [a signal to the New Horizons craft has to travel 50.25 AU and is 7.5M km wide by the time it arrives](https://twitter.com/jpmajor/status/1363565065589448704?s=21), and NASA is pushing software updates over that link!  I can’t even get the Netgear ORBI router next to me to upgrade firmware correctly.  

## IoT

The [Netgear ORBI](https://twitter.com/NetgearOrbi) install has been beyond frustrating. I would have preferred to get EEROs but they were backordered on Amazon (update: getting from BestBuy this week).  The ORBIs require a multistep pairing process with phone and router and satellites, and then they did a firmware upgrade, and then everything was broken.  iOS said it was on the ORBI wifi, but the ORBI iOS app claimed it was not.  No amount of reboots of modems or ORBIs or phones could fix this.  I also tried to factory reset the ORBIs but that solved nothing.  My ISP is Spectrum, I am wondering if Spectrum does some mac-address validation as I was replacing a Spectrum-supplied wifi router.  But Netgear should handle this or at least point me in the right direction.  The ORBIs are in the garage in their box now, I am going to gift them to someone I hate.  

IoT device software is hard — routers, consumer devices, cars, factory devices, all of these are hard devices to provision, to manage, to access.  The industry has made some progress -- it is way easier to install and provision a new device now than it was 3 years ago! -- but many problems seem still largely in front of us:

- Secure registration of devices.  The ORBI experience is not atypical sadly.  I did recently install some Logitech cameras just using Apple’s Homekit app and that seemed to go much better.
- Dynamically pushing software to the edge.  Updates are too clumsy, too heavyweight, too error prone.  There is no simple way to do app upgrades on edge devices.
- Privacy of user data.  Many solutions just throw data up to the cloud, and thus the horse is out of the barn.  We need to figure out how to push code easily to the edge so that data stays in place. 
- Reasoning across incomplete, inconsistent, sampled data.  IoT devices are not always connected, do not provide uniform data sets, have continually varying schemas.  Most analytic solutions want a much cleaner data set that is never going to exist.

## Development and Thinking Tools

I am getting my feet wet as a developer again.  Python, and learning a little bit of Rust and Cargo — wow I love and hate modern package management.  I wanted to read a CSV file, so I imported the Rust CSV library, and ~15 libraries came whizzing in with it.  It is awesome that I can tap into the ecosystem this easily.  But where did all these come from, who wrote them, who maintains them?

On a somewhat related front, Vlad has introduced me to [Nix](https://nix.dev/index.html) which seems like an interesting way to manage development environments. It didn't take me even a couple hours to be completely tangled up in Homebrew, Python, and VSCode. As [Sam](https://twitter.com/sammck) points out, Homebrew just leaks too much globally (and vice versa).

In response to my whining about how to manage my own IP and research, [CharlesF](https://twitter.com/charlesfitz) suggested [Roam research](https://roamresearch.com), and [Prady](https://twitter.com/pradym) pointed me towards [NENO](https://github.com/SebastianZimmer/neno). Roam might be more my thing right now, tho neither does quite what I want.

## Random

I did not know that [snow-to-liquid ratios](https://twitter.com/vortexjeff/status/1361050451148439552?s=21) were a thing. Probably because I am not a skier these days.
