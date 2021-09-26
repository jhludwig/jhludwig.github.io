---
title: "Calculating Pneumatic Cylinder Velocity"
date: "2003-03-20"
tags: 
  - "halloween"
---

**Calculating Pneumatic Cylinder Velocity**. [John](http://aircylinders.netfirms.com) was nice enough to share with me some practical calculations for determining velocity and size of an air cylinder. This is kind of long but I want to save it here for myself...a wealth of practical knowledge here.

Velocity is dependent on flow.

> **S = (Q x 144 x 12)/(A x 60)**, where
> 
> > S = speed, in/sec Q = flow, cubic ft/min A = piston area in sq inches 144 = 144 sq inches per sq foot 12 = 12 inches per foot 60 = 60 seconds per minute

For example,

\* say you have a Parker 1.25DXPSS-8.00, 1 1/4" bore. \* Area is 1.2 sq inches. \* At 1 cubic foot per min, that cylinder will move at:

> (1 x 144 x 12)/(1.2 x 60) = 24 inches per second

\* That says your 8" stroke cylinder extends in 1/3 a second. In practice, it will take a little longer depending on the force available to accelerate the load. More on that later.

So, here's the quick and dirty: **size your cylinder to produce twice the force needed to balance the load (20lb load, provide 40lbs force) and unless you have a really big cylinder or your supply lines are very long (over 200') or very small (less than 1/4"), you'll be fine.**

More gorey details below.

Pressure plays a part in a couple of ways. The first is in overcoming the resistance to flow in your air lines to produce the given flow rate you want. The higher the flow, the greater the pressure drop. So you may have 60psi available at your compressor but at the end of your 100 ft of 1/4" tubing, only 30psi at a flow of 1 cubic foot a minute. (I'm only making these numbers up. I don't know the actual values for this situation, just trying to illustrate the point. )

The second way pressure plays a part is in providing the force to accelerate the load. Say you have a 20lb load. That cylinder needs 20/1.2 = 17psi just to balance the load. At that pressure, it will not lift it, it will only keep it from dropping. You need more pressure than that to accelerate it upwards. If you had 30psi available at the cylinder, it would produce 30 x 1.2 = 36lbs force. So you'd have 36 - 20 = 16 lbs of force available to accelerate the load.

If either of us remembered our physics, we could calculate the rate of acceleration but we'd have to convert lbs to mass and some other ugly stuff. The easy way to do this is to make sure you can produce double the force needed to balance the load (20lb load, provide enough pressure to produce 40lbs force by the cylinder). And as you can see from the example above, unless you're talking about a big cylinder being fed by a tiny (or very long) line, the time to extend the cylinder is next to nothing. Most times, you have to put some kind of flow control on the outlet to slow the cylinder down to keep from slamming it too hard.

In my haunt this past year, I had 12 cylinders going. Each about 1 1/4" bore. All were fed from about 150' of 1/4" tubing. I set my pressure at the compressor regulator to give me 60psi. All my cylinders extended in about a second.

The only time I've had trouble is with homemade cylinders. I made some out of PVC a couple of years ago. They leaked so bad, my compressor ran almost non-stop.
