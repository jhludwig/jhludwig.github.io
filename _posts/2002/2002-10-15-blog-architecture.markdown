---
title: "Blog Architecture"
date: "2002-10-15"
tags: 
  - "tech"
---

**Halloween Blog Architecture**. I am toying around with [blosxom](http://www.raelity.org/apps/blosxom/) for my halloween blog. i like the innate categorization in blosxom as the defining paradigm since my halloween blog is less about dated posts and more about categories of things. getting blosxom running on win2k is proving to be something of a chore. the base scripts have a lot of assumptions about file system naming and file system functionality that are just broken on iis and nt. I have fixed some of this in my [trial blog](http://www.theludwigs.com/Halloween/blosxom.cgi) -- notably i have changed the blosxom scripts to eliminate their expectation of symbolic links (tho i would like to go back and add in windows shortcut functionality as a replacement). The permalinks are busted tho, as there are some differences in cgi handling in iis vs apache. So still tuning -- if anyone has already solved the problem of blosxom on nt, please send me a note!
