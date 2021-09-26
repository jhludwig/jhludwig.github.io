---
title: "Weekend Software Project -- Audio classification"
date: "2016-09-19"
---

This weekend I experimented with some audio classification tools. It was an up and down experience.

I'm interested in a couple features -- hotword detection ala "Hey Siri", "Alexa"; sound event detection (i.e. identify a glass break or gunshot); and acoustic scene classification. I didn't dig into general speech reco, I've dabbled with that in the past.

I experimented with two projects this weekend -- the [Kitt.AI Snowboy hotword detection tool](https://github.com/Kitt-AI/snowboy) and the [DCASE 2016 baseline system](https://github.com/TUT-ARG/DCASE2016-baseline-system-python). I spun up a single docker container that hosted both projects. This was a bit of a PITA, mostly due to getting sound devices to show up in a container. I should post something separate just on that adventure.

Ultimately I got them both working. The Snowboy detector works reasonably well with their universal model; the personal models you can create work also, tho they are not speaker independent. The DCASE code also spins up and training can be done on a standalone machine in a modest amount of time. Unfortunately, both these projects have very restrictive licenses, which makes them kind of useless for anything besides a weekend project.

At the root of almost all these systems is a common feature extraction algorithm, MFCC extraction. MFCCs are explained reasonably well [here](http://www.practicalcryptography.com/miscellaneous/machine-learning/guide-mel-frequency-cepstral-coefficients-mfccs/) and the author provides a [python reference implementation](https://github.com/jameslyons/python_speech_features) with an MIT license. I'm inclined to dig more into this path going forward.
