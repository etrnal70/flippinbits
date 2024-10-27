---
title: "Finally, a Homelab !"
date: 2024-02-02T13:45:15+07:00
draft: false
---

# Background Story

When i was in high school, i've always dreamt having a cool gaming PC with all those fancy 
RGB stuff, liquid cooling and shiny GPU. Fast forward to being a CS students, especially
since familiarizing myself with Linux, all those gaming things loses their cool factor.
Scrolling through *r/homelab* makes me think, '*damn, all those loud rack of computers seems
hella fun !*'.

Another fast forward to 2024, and i finally got my whole minimal homelab setup. For around $350
i've got myself these components:

	- 8U Server rack ($120)
	- TP-Link SG-1016PE Switch ($48)
	- Nano Pi R2S ($48)
	- Google WiFi AC-1304 ($20)
	- ThinkCentre M93p - i7, 16GB RAM, 512GB SATA SSD ($110)
	- Some additional RJ45 cables

## Network

My plan for the switch is to separate existing home network using VLANs. The Nano Pi R2S will
serve as the main router, replacing my Redmi AC2100. My usecase for the router will be VLANs,
DoH, adblocking and VPN connection using Tailscale. The Redmi router will just serve as a dumb
AP for home use, and the Google WiFi will be used for homelab AP.

## Server

I found a good deal for a secondhand M93p at my local online store. 4 cores, 8 thread Haswell
architecture should be more than capable for just running some web applications. The problem
would be limited storage space, since i can only use a single SATA slot. But that shouldn't be
a problem as i aim to add another machine in the near future.

I use Proxmox to manage my VMs and containers. This is a first for me, and haven't setting up
more complex configuration like using Ceph or high-availibility feature, i found it quite
powerful to manage multiple services. I wish i had learn about Proxmox earlier. Next step would
be to make some templates and Ansible configuration to ease service setup.

## Conclusion

So far, i've managed a file server, a GitLab instance for personal projects along with it's CI
runner, and a development VM. Just by setting up all this, i already learn a lot about networking
and maintaining infrastructure. I will update my homelab setup in future posts.

