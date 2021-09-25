---
title: "Win Server 2003 Upgrade problem and fix"
date: "2003-06-10"
tags: 
  - "status"
---

Pings are working again from my blog, I had a rocky week this week. I upgraded to Windows Server 2003 last week -- why? Well, it just seemed like a fun thing to do. Plus I know how fast Microsoft dev resources migrate away from old platforms to the new platform, if you want great ongoing help and support you need to bite the bullet and run the latest stuff.

But the upgrade initially hosed me. The IPSEC service failed to load with a really vague error message, and when IPSEC doesn't load it takes the machine off net. You can turn IPSEC off, but critical services like DNS Client depend on it. For a week I limped along with IPSEC off, and my web server worked, but the machine couldn't do any client name resolution (among other problems) and so trying to ping DNS names didn't work.

Thanks to the responsiveness of guys at Microsoft -- Dave, Jawad, Stephen, Raymond, David, Osman, and more -- we got it figured out. I had installed [Port Explorer beta](http://www.diamondcs.com.au) a long time ago and had quit using it. But it installs Winsock providers and these were hanging around on my system -- we discovered these by using the sporder.exe tool from the [windows platform sdk](http://www.microsoft.com/msdownload/platformsdk/sdkupdate/). On an upgrade to WinServer2003, these make IPSEC unhappy, it refuses to load, and things go to sh%t.

Once I uninstalled Port Explorer, things righted themselves.

I tried to use the online Microsoft support options to get this resolved -- the KB, the support forums -- but there was no info about, and the folks in the support forum just told me to reinstall. Thankfully the dev teams at Microsoft were super responsive. Thanks much guys!
