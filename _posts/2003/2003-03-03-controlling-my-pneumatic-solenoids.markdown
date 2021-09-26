---
title: "Controlling my pneumatic solenoids"
date: "2003-03-03"
tags: 
  - "halloween"
---

**Controlling solenoids**. As i plan my pneumatic system, I need some way to control my solenoids. I am thinking about possibly a midi-based system, and need a device that converts midi wiring/protocol to the 12/24v required by most solenoids. [Mediamation](http://www.mediamat.com/) seems to make such gear. Another one from [Laserium](http://www.laserium.com/hardware/MIDIana.html) tho it only support signals up to 10V. The Gilderfluke [Servo controller](http://www.gilderfluke.com/gilderflukepsfiles/CutSheets/SER-DMX.pdf) or [analog brick](http://www.gilderfluke.com/gilderflukepsfiles/CutSheets/BR-ANA.pdf) may do the trick, but using DMX digital input instead of MIDI -- but this is ok, my control software is native DMX anyway -- I have email into gilderfluke requesting advice.

Update: nice mail from the gilderfluke folks:_Are your valves analog or digital (just on off)? If they're analog, then, yes, you are correct. The BR-ANA card will fit the bill. If they're digital, either the MultiBrick32 or our Zbricks would do nicely. I recommend the more expensive MultiBrick 32 because it has a microprocessor that is able to filter out the occasional bad packet of DMX. If your application doesn't have a critical need to prevent the occasional "hiccup" (1 or 2 frames worth) and the valves are digital, then the Z-Bricks are a very cost effective solution._

Another DMX alternative is a [Dove Analog Dimmer](http://www.dovesystems.com/BuildPage.php?page=mtx). I use Dove dimmers now for my 120V and 240V gear (lighting and fog systems) and I have been happy with their sturdiness. $795 for the unit I want.
