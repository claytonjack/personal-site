---
title: "Elevating My Home Network With pfSense"
date: 2023-09-01T06:00:23+06:00
hero: images/hero/networking.jpg
description: "My home router and firewall solution."
theme: Toha
menu:
    sidebar:
        name: "Pfsense Router/Firewall"
        identifier: networking
        weight: 500
---

### Introduction

Shortly after acquiring my initial server, it became evident that my home network required a more robust solution. Up until that moment, I had relied on the all-in-one router provided by my ISP for years. However, my evolving needs prompted a change. As I ventured into hosting services for both personal use and others, I soon recognized the inherent limitations of consumer-grade hardware. Not only are these devices slow, but they also lack advanced features like VPN support and seamless backup capabilities.

{{< img src="/posts/images/home-network/modem.jpg" height="400" width="600" align="center" title="Modem" >}}

### Software Options

When faced with the choice of selecting the ideal firewall/router software for my needs, I knew I wanted a solution that could run on my own hardware. Today's landscape offers a plethora of choices with some of the more popular options being pfSense, OPNsense, Sophos, and Untangle. Ultimately, I decided to go with pfSense, primarily due to its reputation for reliability and the extensive resources that are available online.

{{< img src="/posts/images/home-network/router-software.png" height="400" width="600" align="center" title="Router Software" >}}

### Original Configuration

Initially, I chose to set up pfSense as a virtual machine. At that point, I had been heavily relying on containers and wanted to gain some hands-on experience working with virtual machines. I was aware of the logistical concerns that might arise by hosting both my router and [primary server](https://claytonjack.com/posts/server-software/server-software/) on the same hardware. To mitigate these concerns, I opted to set up a separate machine running Proxmox with pfSense as the sole production VM. This configuration served me well for many years, offering both rock-solid reliability, as well a safe place to experiment with other virtual machines.

{{< img src="/posts/images/home-network/pfsense-vm.png" height="400" width="600" align="center" title="pfSense VM" >}}

### Tiny/Mini/Micro Hardware

This year, I made some major changes to my overall infrastructure as discussed [here](https://claytonjack.com/posts/server-software/server-software/), what this meant for my router was that it was time to move to dedicated hardware. Due to my [extensive experience working with hardware](https://claytonjack.com/posts/server-hardware/server-hardware/), I decided to once again go with a custom solution. Vendors like Dell, HP, and Lenovo boast an extensive array of offerings in the "Tiny/Mini/Micro" category of desktop computers. These machines are a favored choice with businesses due to their space-saving design and for being cost-efficient. These machines are often procured in bulk and subsequently rotated out every few years, meaning there is always a large supply available on the used market. This ease of availability and discounted prices have led to these computers becoming very [popular in the homelab community](https://www.servethehome.com/introducing-project-tinyminimicro-home-lab-revolution/) as routers or as part of a cluster.

{{< img src="/posts/images/home-network/router-exterior.jpg" height="400" width="600" align="center" title="Router Exterior" >}}

### Current Hardware

The Lenovo ThinkCentre M720q emerged as the sole contender that aligned seamlessly with my requirements. I desired a machine that excelled in acoustics, consumed minimal power, and occupied as little space as possible. I also had a mandatory requirement of PCIe expansion capabilities to support the addition of a dual port NIC. Currently, Lenovo is the only vendor that offered all of the features that I required, with the M720q being the first model to do so through the use of a proprietary PCIe riser card. If I wanted a machine this small, then this was my best option.

{{< img src="/posts/images/home-network/router-interior.jpg" height="400" width="600" align="center" title="Router Interior" >}}

### Current Software

Once I had the hardware in place, migrating my existing configuration was simple due to the built-in backup and restore function that pfSense offers. My use case for pfSense is relatively simple compared to what you would find in a business environment. The main features that I utilize are static DHCP mappings, port forwarding for temporary game servers, pfBlockerNG, and Tailscale VPN.

{{< img src="/posts/images/home-network/pfsense-dashboard.png" height="400" width="600" align="center" title="pfSense Dashboard" >}}
