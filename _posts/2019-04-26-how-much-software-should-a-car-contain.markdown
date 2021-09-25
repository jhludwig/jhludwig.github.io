---
title: "How much software should a car contain?"
date: "2019-04-26"
---

In a [recent article about the latest VW Golf,](https://www.autoblog.com/amp/2019/04/25/mk-8-vw-golf-software-issues/) the product manager was quoted "Already now there are ten times more lines of code in the latest Golf than in a smartphone". This statement is interesting in some many directions.

Software content in a car is growing exponentially as connectivity, autonomy, sensors, new compute platforms, electrification all drive into the car and this VW metric is an interesting indicator.

But is that too much software? It seems like my cellphone is jammed full of software, does my car really need 10X the lines of code?

But then the car has at least two major compute domains (UX and drive control) with many smaller compute loads, and maybe it is reasonable to have a lot more software than a smartphone?

Is KLOCs the right way to measure software? That is an '80s way of thinking about software content and leads to some very bad behavior. Should anyone be proud of this?

What is the quality level of that software? Modern smartphones and the services that power them have the most highly compensated people in the industry banging away on them. How should we feel about a software system with 10x the number of components but with less highly compensated engineers? What is the total lifetime cost of all that software? What is the security exposure of all the software?

The biggest challenge VW is struggling with is OTA updates per the article. The OTA challenge in a car is broad -- firmware, headunits, apps all have their own lifecycles and OTA needs. Is there an understanding that a great architecture for OTA and application isolation in the car are probably the first things that should have been put in place?

How much software should be on your mobile phone and in the cloud to support your driving? More or less than is in the car itself? How does that change when your car is always connected?

It is fascinating time in the auto industry. Software content is growing by leaps and bounds. While the VW number may be too high today, there is going to be a LOT more software content in cars over time.
