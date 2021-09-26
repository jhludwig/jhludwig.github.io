---
title: "XP Server, IIS, DNS Client"
date: "2004-12-10"
categories: 
  - "blog"
---

For some reason, about two weeks ago, my IIS server (that this site resides on) quit being able to resolve DNS names. I've tried changing my DNS servers, no avail. I've tried turning off and turning on the DNS Client Resolver, no avail. The only config change I have made recently is to turn on the WebDAV extension in IIS, I turned that off, no avail.

This happened to me when I first installed XP Server 2003 and it was due to a 3rd-party socket filter that i had to remove. Going to investigate that next. Also going to look at ways to log the traffic at the IP level as i try to hit a named site to see what is happening.

Static pages on the site work fine obviously, but any kind of dynamic page tends to fall over.

Maybe it is time to move to a hosted solution. Not really having fun chasing this crap down.

**UPDATE**: used the Network Monitor utility in XP to see that, for whatever reason, the DNS servers I had been using were returning "name not found" to all my requests. Further dug in and found that our ISP had provided us new DNS servers to use for our DMZ boxes a couple weeks ago. All fixed up now. Don't really understand why the old DNS servers were still operational and still responding to DNS requests at all, but onward and upward.
