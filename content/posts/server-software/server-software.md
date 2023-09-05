---
title: "Server Software"
date: 2023-08-04T06:00:23+06:00
hero: /images/posts/writing-posts/analytics.svg
description: My server software.
theme: Toha
menu:
    sidebar:
        name: Server Software
        identifier: server-software
        weight: 500
---

### Original Setup

Until recently I had been using Unraid as the operating system of choice for my server. Unraid is known for being very beginner friendly and for offering a great WebUI. This fit my needs perfectly at the time as the world of Linux servers was very new to me. The issue for me however was that I wasn't learning enough about how elements like Linux, Containers, and Virtual Machines truly worked. It was easy to follow guides and get things working but I was lacking the deeper understanding. Over time, I started to pick up enough until my knowledge reached the stage where I was ready to make a switch.

### Proxmox

My plan was to use a standard Linux VM to run the majority of my services. Therefor, I wanted a Hypervisor that was solely focused on running virtual machines well. Right away, I narrowed my options down to Proxmox and VMware ESXi. I ended up choosing Proxmox mainly due to less restrictive licensing and its popularity in the homelab community.

### Storage VM

For mass storage, currently I have an array of five 6tb WD Red drives with one of them being dedicated to parity. These drives are attached to a LSI HBA card which has been modified to run in IT mode. Doing this removes the RAID functionality of the card but allows each individual drive to be seen by the host operating system which is exactly what you want for a [JBOD Array](https://en.wikipedia.org/wiki/Non-RAID_drive_architectures#JBOD). It mode allows for the. For now, I have kept the array intact on Unraid but have transitioned to running it as a VM on Proxmox instead. Unraid boots the operating system from a USB drive which made this process quite simple as all I needed to do was pass the USB drive through to the VM. However, this is still a temporary solution as I plan to eventually migrate to using either a combination of SnapRAID and MergerFS or TrueNAS for a more robust solution utilizing ZFS.

### Ubuntu VM

My Ubuntu Server VM is

### Remote Access

-   Plan to move to AWS

### Conclusion / Future Plans
