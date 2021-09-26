---
title: "Credit card fraud and reverse DNS"
date: "2006-11-08"
tags: 
  - "security"
---

We had a credit card stolen a while back and I was just on the phone with the bank clearing up one last transaction. The vendor, [Steam](http://www.steampowered.com/v/index.php), was claiming that the charge was valid. It took me about 2 minutes to convince the card issuer that the charge was not valid by simple reverse DNS of the IP addresses captured by Steam. Account signup happened at a location served by Adelphia (I have never been an Adelphia customer), and subsequent accesses all took place via two different Russian ISPs.

What surprises me is that neither Steam nor the card issuer (a huge national card issuer) was able to figure this out. It seems very automatable. And seems like card issuers could easily cut down on online fraud by looking at IP addresses -- for myself, 99.99% of my transactions come from my work or home machines with fairly stable IP address histories, at least at the subdomain level. Not foolproof of course, and I do occasionally do transactions from other locations, but it seems like another good piece of info to consider when assessing the validity of a particular transaction.
