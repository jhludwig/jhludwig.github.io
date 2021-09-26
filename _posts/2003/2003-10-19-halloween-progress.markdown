---
title: "Halloween progress"
date: "2003-10-19"
tags: 
  - "halloween"
---

Been very busy with my pneumatic cylinders, solenoids, compressors, and the control electronics for all the above. finally this AM i got my coffin to open under computer control! happy but tired.

Some things I learned/relearned along the way:

- Assembling pneumatic circuits and electrical circuits is NOT like building a spreadsheet in Excel. You can't just start whacking parts together. You actually have to pay attention to load requirements, total system capacity, etc. And connector types! If you just try to whack things together, prepare yourself for lots of wasted parts and lots of unnecessary trips to various suppliers. Planning is essential.
- Don't try to finesse pneumatic and electrical loads -- use bigger components so that you don't have to worry about whether you met the amperage requirement or not. Better to have 5x oversupply than to come up 15% short.
- KISS. When you have multiple solutions available, use the simple one. It may be attractive (and more elegant) to figure out how to build an electrical circuit that decodes DMX512 signals, converts them to 10V analog signals with sufficient amperage to control a solenoid. But it is a lot easier just to hook the solenoid up to AC and to switch the AC on and off under computer control, there are many widely available solutions to turn AC on and off.

Anyway my coffin is reliably opening and closing in a scary erratic way, should be fun on Halloween night.
