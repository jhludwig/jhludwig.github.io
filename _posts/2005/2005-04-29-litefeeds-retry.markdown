---
title: "litefeeds retry"
date: "2005-04-29"
tags: 
  - "software"
---

I previously posted that I tried [litefeeds](http://www.litefeeds.com) and it didn't work. [One of their developers](http://www.litefeeds.com/blojsom/blog/john/) read my blog and contacted me for details, and so I retried.

I am happy to say that litefeeds now works fine, and there was never really a problem except for a rookie mistake by me.

I read my subs using [newsgator](http://www.newsgator.com), and I regularly export the OPML file from newsgator to [blogrolling.com](http://www.blogrolling.com) for my blog's sidebar. Blogrolling.com will export my blogroll in opml as well, and I grabbed that for importation into litefeeds, blithely thinking "hey all opml files are the same". WRONG. The newsgator exported file contains RSS feed urls. When imported into blogrolling, blogrolling determines the base blog url and just saves that. And so the exported opml file from blogrolling is not rss feed urls, but blog urls.

So litefeeds works fine now. And now that I can play with it I have some more constructive comments. It does install nicely and has a small memory footprint. But it is too hard to see content. First, when I have a feed or item listed, the space bar or return key should perform the default action -- open the feed and show me the posts, open the post and show me the content.

Second, I don't want just the entry excerpt provided by the feed, I want to push thru and read the whole post -- litefeeds should integrate with the blackberry browser and let me read the posts.

So...happy to report that litefeeds works, and appreciate the support from the team. Hoping that they will add some more features so that it is even easier to read content.
