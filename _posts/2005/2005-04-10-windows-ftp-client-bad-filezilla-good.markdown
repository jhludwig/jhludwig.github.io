---
title: "Windows FTP client bad, Filezilla good"
date: "2005-04-10"
tags: 
  - "software"
---

Reminded again this week how crappy the built-in ftp client in winxp is. Struggled for a day with uploading some simple cgis to a hosting service before it dawned on me that the xp client was sending them in binary mode, not ascii. I upload cgis to a windows server all the time using the xp client, apparently msft does something special between xp clients and windows servers to fix up the uploads because I never had a problem with this config.

And the builtin client doesn't have a way to force ascii or binary, at least not that I could find.

"Filezilla":google proved to be a great answer. Reasonable browsing ui, automatically handles ascii/binary selection for most files, handles disconnects/reconnects well.
