---
layout: post
status: publish
published: true
title: Toying with disaster. Auto Updater and UAC Control.
author:
  display_name: Jonathan
  login: jmhadmin
  email: jmh@jonathanhardison.com
  url: ''
author_login: jmhadmin
author_email: jmh@jonathanhardison.com
wordpress_id: 314
wordpress_url: http://www.jonathanhardison.com/index.php/2009/10/28/toying-with-disaster-auto-updater-and-uac-control/
date: '2009-10-28 12:07:02 -0500'
date_gmt: '2009-10-28 18:07:02 -0500'
categories:
- Uncategorized
tags: []
comments: []
---
So I'm toying with an auto update feature that I will embed into the little apps I write. Currently I'm testing out how to detect forced manual updates and full local installers, as opposed to just a quick file patch. But in the process I found that I need to advertise myself for elevated privileges with UAC to perform updates on Windows 7. So the code to do this can be found over [here](http://www.aneef.net/2009/06/29/request-uac-elevation-for-net-application-managed-code/){:target="_blank"} Basically you are modifying your applications manifest, and then checking the level in the app through a function to ensure you have it.
