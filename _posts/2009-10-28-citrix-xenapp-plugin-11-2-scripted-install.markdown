---
layout: post
status: publish
published: true
title: Citrix XenApp Plugin 11.2 Scripted Install
author:
  display_name: Jonathan
  login: jmhadmin
  email: jmh@jonathanhardison.com
  url: ''
author_login: jmhadmin
author_email: jmh@jonathanhardison.com
wordpress_id: 311
wordpress_url: http://www.jonathanhardison.com/index.php/2009/10/28/citrix-xenapp-plugin-11-2-scripted-install/
date: '2009-10-28 11:48:01 -0500'
date_gmt: '2009-10-28 17:48:01 -0500'
categories:
- Uncategorized
tags: []
comments: []
---
I had to revisit an old installer I had made that relied on a script running in the background for some additional software to be installed. This script also did a little cleanup of shortcuts, etc. I have since changed it all to run in InstallScript, however, this particular visit I didn't want to change it over to the new install. My problem is the installer for Citrix has gone through a drastic change. But never fear, the command line is super simple.

CitrixOnlinePluginFull.exe /silent ADDLOCAL="ICA_Client,SSON,Flash,USB,DesktopViewer"

Now you also need to know that PN.exe is officially gone in this release, so if you need the functions of that program, you can get the Citrix Quick Connect Tool to perform the same functions. But in a more RDP style screen.

![img]({{site.base}}/imagecontent/2009/10/Capture8.png)

![img2]({{site.base}}/imagecontent/2009/10/Capture9.png)

Download the Quick Launch from [link](http://support.citrix.com/article/CTX122536){:target="_blank"}
