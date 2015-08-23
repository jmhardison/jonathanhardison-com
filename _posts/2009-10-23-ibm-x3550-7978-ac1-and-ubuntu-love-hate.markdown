---
layout: post
status: publish
published: true
title: IBM x3550 7978-AC1 and Ubuntu&hellip; love hate?
author:Jonathan
author_login: jmhadmin
author_email: jmh@jonathanhardison.com
wordpress_id: 306
wordpress_url: http://www.jonathanhardison.com/index.php/2009/10/23/ibm-x3550-7978-ac1-and-ubuntu-love-hate/
date: '2009-10-23 07:36:09 -0500'
date_gmt: '2009-10-23 13:36:09 -0500'
categories:
- Uncategorized
tags: []
comments: []
---
Repurposing an old server as a Linux server to handle general functions is great. But what if you have a 7978-AC1 pile of turd and you want the latest Ubuntu Server on it?

In my particular case, the 7978-AC1 would load 8.04TLS just fine, but would hang if I tried to install 8.10 or 9.04 directly. So the resolution is as simple as it gets. (maybe a BIOS update would help, but I like finding the hard way first.)

1. Install Ubuntu 8.04TLS.
2. Apt-get install update-manager and change it's config to do normal releases. ( /etc /update-manager /release-upgrades and set Prompt=normal)
3. Perform the upgrade from 8.04 to 8.10. (sudo do-release-upgrade)
4. Perform the upgrade from 8.10 to 9.04. (sudo do-release-upgrade)
5. Enjoy.

That's the long way around the problem; but I like knowing worst case scenarios.
Now move on to your GroundWork Open Source install and be happy.
