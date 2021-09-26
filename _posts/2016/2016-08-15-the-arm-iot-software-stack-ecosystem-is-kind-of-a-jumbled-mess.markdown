---
title: "The ARM IOT software stack ecosystem is kind of a jumbled mess"
date: "2016-08-15"
---

Google has announced [Brillo](https://developers.google.com/brillo/) which leverages Android and Linux. But no, wait, now there is [Google Fuchsia](https://www.engadget.com/2016/08/13/google-fuchsia-operating-system/) because apparently Linux isn't good enough. On the pi there are a jillion variants of linux to use, but with glaring holes (general purpose gpu, docker for instance). ARM has [mbed](https://www.mbed.com/en/platform/mbed-os/) tho it is really targetted at low end devices. You can try [Windows 10](https://developer.microsoft.com/en-us/windows/iot). And all of these require a lot of laborious tinkering.

To say nothing of the cloud, the services for managing ARM devices are even more nascent or non-existent.

You have to wonder what Softbank is going to do about this. A $32B hardware bet needs a corresponding software and services bet.

UPDATE: [Nat](https://twitter.com/natbro) reminds me that I didn't even mention toolchains! Cross-compilers, QEMU, etc -- there is so much fun in here!
