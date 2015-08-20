---
layout: post
status: publish
published: true
title: UVerse TV and the case of the bloats.
author:
  display_name: Jonathan
  login: jmhadmin
  email: jmh@jonathanhardison.com
  url: ''
author_login: jmhadmin
author_email: jmh@jonathanhardison.com
wordpress_id: 641
wordpress_url: http://www.jonathanhardison.com/?p=641
date: '2011-11-24 19:51:47 -0600'
date_gmt: '2011-11-25 01:51:47 -0600'
categories:
- Uncategorized
tags: []
comments: []
---
<p>So in a normal brain fart moment, I failed to remember several of my own teachings when adding a second Access Point to my home network. You see, I have ATT UVerse TV service at home, and for those who don't remember it uses IGMP to multicast the TV feeds to the receivers. So if you for example, have a receiver plugged directly into the 2Wire modem, it will send the traffic out that port. Now, if you have that receiver plugged into a switch and share the drop with other devices it still comes down that line, however the switch more than likely does not understand multicast. Unless you have a more expensive device in there that is.</p>
<p>But here's how this works. A packet that is a multicast packet, the first part of your MAC address will be a 01. If a switch understands multicast packets, then it will deliver that packet out the port of the device that is part of that multicast group. (IGMP Group). Now lets say you have a switch that doesn't understand it, know what it does then? Yup, it treats a multicast packet as a broadcast packet and sends it out all ports but the one it came in on.</p>
<p>Now, lets say you have a brain fart moment and forget this and try to plug an access point off a line that has a receiver. Guess what happens to that access point... Well the short story is you will see it work... until you try to connect to it. There would be so much data trying to hit the wireless that your connection will time out.</p>
<p>So you have a couple fixes.<br />
1. Reshuffle your network so that there is nothing on the same line as the receiver.<br />
2. Run additional cables.<br />
3. Replace your switches with ones that support IGMP&#47;Multicast.<br />
4. VLAN your network, and isolate the receivers. (Which would also imply either your switches all support this or you ran more drops.)</p>
<p>or if you are me...</p>
<p>You run new drops, replace your core switch with a more business minded switch that supports multicast, and you VLAN your network and isolate the receivers. Then you go further and trunk the line to your AP's so you can send a VLAN to a specific wireless SID and make it a public hot spot.</p>
<p>Oh the wife will not like me today. ;)</p>
