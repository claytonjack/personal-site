---
title: "Synology to DIY: My Hardware Journey"
date: 2023-09-02T06:00:23+06:00
hero: images/hero/hardware.jpg
description: "My server hardware history."
theme: Toha
menu:
    sidebar:
        name: "Server Hardware"
        identifier: server-hardware
        weight: 500
---

### My First NAS

My journey into the world of home servers and self-hosting began in 2016 with a modest Synology NAS. As someone who has always had an interest in collecting things, my passion continued into the realm of technology. As you start to accumulate files, managing them starts to become an issue and you start looking for a better way to stay organized. It was at this moment where I began looking at prebuilt NAS solutions, before eventually settling on the Synology DiskStation DS415+. This NAS served as an excellent entry point, introducing me to the exciting new technologies like SMB and RAID that I had yet to explore.

{{< img src="/posts/images/server-hardware/synology-nas.jpg" height="400" width="600" align="center" title="Original Server Room" >}}

### Synology Failure

Nonetheless, the durability of this setup was disappointingly short-lived. In 2019, shortly after my warranty had lapsed, my unit encountered a sudden failure that rendered it inoperable. After some research, I discovered that this was a widespread issue plaguing a wide range of products. The issue stemmed from a [design flaw in Intel Atom C2000 series chips](https://www.anandtech.com/show/11110/semi-critical-intel-atom-c2000-flaw-discovered) which caused premature failures without a hardware fix. Regrettably, Synology offered no support, leaving me with no choice but to attempt a DIY repair. Luckily, the fix proved to be relatively simple, all that was required was the [soldering of a 100 Ohm resistor](https://www.sciuro.org/posts/2020/03/repairing-a-synology-nas/) onto the motherboard.

{{< img src="/posts/images/server-hardware/synology-fix.png" height="400" width="600" align="center" title="Synology NAS Fix" >}}

### Custom Built Server

While my repair proved successful, I had doubts about its long-term reliability. With my data at stake, I chose not to take the gamble and opted to migrate to a more reliable solution. This migration also offered me the opportunity to bolster the processing power of my server. Due to extensive experience building custom computers in the past, I am very comfortable working with hardware. This, in addition to having a clearer understanding of how servers work, led me to decide to build my own. I fully acknowledge that in the enterprise space, performance isn't the sole determining factor. Reliability, support, and security are often heavily considered by businesses before deciding on hardware. I aimed to incorporate as much enterprise-grade hardware as possible, which provided access to features I deemed important like ECC memory and IPMI. Eventually, settling on the following.

{{< img src="/posts/images/server-hardware/custom-server.jpg" height="400" width="600" align="center" title="Custom Built Server" >}}
