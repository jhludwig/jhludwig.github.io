---
title: "Docker and VSCode on OS X -- not ready for primetime"
date: "2017-05-22"
---

My workflow for years on my MBP has centered on VMWare running Debian/Ubuntu, and all my tools in the VM.

For developing code targeting AWS services, I thought I'd try using Docker for Mac and running Debian images with Docker.

Well that didn't work. [This bug involving time drift in a container](https://forums.docker.com/t/time-in-container-is-out-of-sync/16566) has been around for a year now, with no attention paid to it. It basically makes it impossible to access any AWS services. I have to conclude that no one is actually using Docker for Mac.

I've also for years used a variety of editors and IDEs on both the Mac and Linux side. I heard such good things about VSCode that I decided to try it. But after any amount of time running it, it starts to miss keystrokes -- I first noticed it wasn't responding to copy/paste from the keyboard, then it also started to fail on simple text entry. I have no time for this, as cool as VSCode may be, it fails on the fundamentals.
