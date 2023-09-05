---
title: "pfSense Router"
date: 2023-08-03T06:00:23+06:00
hero: /images/posts/writing-posts/analytics.svg
description: My home router and firewall solution.
theme: Toha
menu:
    sidebar:
        name: pfSense Router
        identifier: pfsense-router
        weight: 500
---

### Introduction

Not long after receiving my original server, I realized that I needed a more robust solution for my home network. Until this point, I had been using the all in one router provided by my ISP for years but now I had new requirements. Once you start hosting services for yourself and others, you start to realize how limited consumer grade hardware is. Not only are these devices slow, they also lack advanced features like VPN support and seamless backups.

### Software Options

When deciding which firewall/router software I wanted to use, I knew I wanted something that I could run on my own hardware. There are plenty of options these days with the most popular being pfSense, OPNsense, Sophos, and Untangle. In the end, I decided to go with pfSense because of its reputation for being reliable as well as the vast amount of resources available online.

### Original Configuration

At first, I setup pfSense as a virtual machine. At this point, I used containers exclusively for everything and wanted some experience working with virtual machines. I understood the logistical issues that would arise with having my router and [main server](https://claytonjack.com/posts/server-software/server-software/) on the same machine. Instead, I installed Proxmox on a secondary machine with pfSense being the sole production VM. This setup served me well for many years, offering rock solid reliability and a safe place to experiment with other virtual machines.

### Current Configuration Hardware

This year, I made some major changes to my overall infrastructure as discussed [here](https://claytonjack.com/posts/server-software/server-software/). What this meant for my router was that it was time to move to dedicated hardware. Due to my [extensive experience working with hardware](https://claytonjack.com/posts/server-software/server-software/), I decided to go with a custom solution. Venders like Dell, HP, and Lenovo offer a wide range of products in the "Tiny/Mini/Micro" category of desktop computers. These machines are incredibly popular with businesses due to their low cost and small form factor. Often these machines are purchased in bulk and replaced every few years, meaning there is a large supply available on the used market. These factors have made them very [popular in the homelab community](https://www.servethehome.com/introducing-project-tinyminimicro-home-lab-revolution/) as routers or as part of a cluster. The only desktop that fit my needs was the Lenovo ThinkCentre M720q. I knew I wanted something quiet,low powered and as small as possible. A mandatory requirement however, was PCIe expansion capability to support the addition of a dual port NIC. The M720q is the first model that supports this expandability through the use of a proprietary PCIe riser card. If I wanted a machine this small, then this was my best option.

-   Backup & Restore
-   Tailscale VPN
-   pfBlockerNG
-   Portforwarding for Game Servers (dont keep these open)
-   Static DHCP Mappings
