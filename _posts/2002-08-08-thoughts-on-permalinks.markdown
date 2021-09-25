---
title: "Thoughts on Permalinks"
date: "2002-08-08"
tags: 
  - "tech"
---

**Permalinks** I am trying to decide whether to add permalinks to my site, and if so how to implement them. I have been slow to do so because I take a very long view of what the word "permanent" means. I want to implement a system that will last for 20+ years, during which time i will post a lot of content of all sorts, and i am sure that the system i use to manage content will change dramatically. I don't want to have to recreate my entire naming scheme multiple times, that will kind of defeat the purpose.

I've looked at permalinks on a lot of other sites. There are some mistakes being made. For instance I have seen permalinks of the form "www.foo.com/GUID" where the GUID is 6 decimal digits. Seems like a lot but the history of software shows again and again that you need to allow way more address space than you originally imagine you will need. I've also seen permalinks of the form "www.foo.com/keyword/GUID", with the author sorting their posts into several categories. I predict unhappiness here as categorization decisions and hierarchy will change over time. The right kind of permalink seems to be "www.foo.com/date/guid" which allows unbounded expansion and doesn't embed unnecessary assumptions about categories or namespaces into the permalink.

I have a lot of resources besides just those i post in my blog that i want to be remotely accessible. like files. i wonder if the permalink convention should span them as well. the timestamp is a lot less relevant for these types of resources.

i wonder if permalinks are right at all. i wonder if a more durable interface is a search interface -- ie a standard search submittal syntax for my site. this seems like it might let me futz with the underlying implementation a lot more.
