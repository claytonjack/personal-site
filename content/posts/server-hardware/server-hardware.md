---
title: "Server Hardware"
date: 2023-08-05T06:00:23+06:00
hero: /images/posts/writing-posts/analytics.svg
description: My server hardware.
theme: Toha
menu:
    sidebar:
        name: Server Hardware
        identifier: server-hardware
        weight: 500
---

### My First NAS

My journey into the world of home servers and self-hosting initially began in 2014 with a humble Synology NAS. Since childhood, I always loved collecting things and this continued when I became interested in technology. Everyone has that voice in the back of their head telling them that some day they will need to access that old podcast episode while offline. At a certain point, you end up with thousands of files and need a way to manage them. At this point, I turned to prebuilt NAS solutions and eventually settled on the Synology DiskStation DS415+. This NAS was a great entry point and introduced me to new technologies like SMB.

### Synology Failure

This setup however would not last long. In 2017, not long after my warranty expired, I experienced a sudden failure in my unit that rendered it unusable. After some research, I discovered that this was a widespread issue with various router and NAS devices and was caused by a [design flaw in Intel Atom C2000 series chips](https://www.anandtech.com/show/11110/semi-critical-intel-atom-c2000-flaw-discovered). Synology refused to offer any support so I went about trying to repair it myself. It turned out the fix was relatively simple, all I needed to do was [solder a 100 Ohm resistor to the motherboard](https://www.sciuro.org/posts/2020/03/repairing-a-synology-nas/). Although my repair was successful, I didn't know how long it would last. I was not willing to risk my data so I decided to migrate to a new solution.

### Custom Built Server

I wanted a machine that offered me more CPU power as well as additional hard drive bays so that the transition wouldn't feel like a lateral step. In my opinion, the prices of high-end prebuilt NAS solutions far exceed the actual value that the product provides. I am also very comfortable working with hardware due to extensive experience building custom computers. This made the decision to build my own server a simple one. I understand that in the enterprise space, performance isn't always king. Each business has its own set of needs, factors like reliability, support, and security are often more important than raw performance. For my new server, I knew I wanted to use as much enterprise-grade hardware as possible in order to enjoy important features like ECC memory and IPMI. In order to keep costs down, I purchased the majority my hardware from eBay and ended up with the following system.

Image/Table: Current server specs
<br>
Image: Current server (not on rack)

### Future Hardware Plans

-   More CPU cores (at least 8 + HT)
-   ECC RAM for ZFS
-   Intel Quick Sync (AV1 consideration?)
-   IPMI (May use PiKVM instead)
-   10Gbe (Maybe 2.5Gbe?)
