---
title: "Startup Processes in Windows"
date: "2002-05-18"
tags: 
  - "tech"
---

**Startup Processes in Windows**. I'm helping my dad figure out how to shut off various strange startup processes in windows. AN incredibly common problem and incredibly stupidly painful to fix. In his case some reminder program about MSN internet service is nattering at him all the time.

The easy steps are to go to the Startup group in the Programs menu and get rid of any gorp you don't want. A legacy from win3.x are the LOAD= and RUN= lines in system.ini.

But there is still a bunch of stuff running. Hmm. Ok now we go registry whacking. Run Regedit. Navigate thru the tree control on the left to the key named HKEY\_CURRENT\_USER\\Software\\Microsoft\\Windows\\CurrentVersion\\Run (at least that is the name on Win2k). Examine the rightmost screen dad. If you're not sure, don't touch! Call me.

Ok now navigate to the key named HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Run. Same dealy.

Finally you may have to look a key named HKEY\_USERS\\\[somelongnumber\]\\Software\\Microsoft\\Windows\\CurrentVersion\\Run. Same dealy.

When you are done, reboot and see if that helps! Oh and here is at least one site that lists the name of [strange tasks](http://www.answersthatwork.com/Tasklist_pages/tasklist.htm) running in the background of windows and if you are supposed to touch them. There are others -- try searching [Google](http://www.google.com) with the name of the strange executable, or [technet](http://www.microsoft.com/technet/default.asp).
