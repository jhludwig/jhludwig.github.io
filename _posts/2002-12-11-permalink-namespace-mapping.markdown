---
title: "Permalink Namespace Mapping"
date: "2002-12-11"
tags: 
  - "tech"
---

**Permalink Namespace Mapping**. I am sure there are solutions to this problem out there. As i futz with the implementation of my blog under the covers, I am causing changes in the permalink namespace for my site, mostly because IIS wants filename extensions to help it figure out which script engine to use, and these filename extensions end up showing up in the namespace. I am sure there is some way to either configure this behaviour out of IIS, or inject some piece of code that does some lightweight name fixup so that my old permalink namespace will always work. Need to dig around on this today.
