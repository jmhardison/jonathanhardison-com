---
layout: post
status: publish
published: true
title: iPhone 2.1 Wi-Fi and Exchange
author:
  display_name: Jonathan
  login: jmhadmin
  email: jmh@jonathanhardison.com
  url: ''
author_login: jmhadmin
author_email: jmh@jonathanhardison.com
wordpress_id: 41
wordpress_url: http://jonathanhardison.com/?p=41
date: '2008-09-29 12:12:41 -0500'
date_gmt: '2008-09-29 18:12:41 -0500'
categories:
- Uncategorized
tags: []
comments: []
---
![mainoverview]({{site.base}}/imagecontent/2008/09/main_overview20080609-268x300.jpg)

Since I made the post on the 2.1 issues I’ve seen, I have been able to narrow down one of the items. Or at least see a pattern when it happens.

The ‘Push’ Exchange feature not working correctly is actually specifically when my iPhone flips to wireless. It is like the wireless is shut off after communications are done, and the phone does not send a state update over the edge/3g network to the exchange server. Basically the push function is a delayed HTTP request. And the server needs to be able to talk back to the phone on the last address the request was created on. When the wireless is shut off, that path is closed.

However, if you keep the phone in the mail section when it sleeps, the funciton will work. Drop back to the main screen, and it stops working after the wireless is shut off.



I will continue to watch this item, but so far, that is what I have found. So here’s to the next patch that will hopefully fix this issue, without breaking anything else!
