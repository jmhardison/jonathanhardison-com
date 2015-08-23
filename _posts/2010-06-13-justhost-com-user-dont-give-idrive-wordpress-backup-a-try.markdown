---
layout: post
status: publish
published: true
title: Justhost.com user? Don't give iDrive Wordpress Backup a try!
author:Jonathan
author_login: jmhadmin
author_email: jmh@jonathanhardison.com
wordpress_id: 523
wordpress_url: http://www.jonathanhardison.com/?p=523
date: '2010-06-13 11:36:59 -0500'
date_gmt: '2010-06-13 17:36:59 -0500'
categories:
- Internet
tags: []
comments: []
---
If you are a user of JustHost.com services, specifically the unlimited plan, as well as a user of WordPress. You should do your best to stay clear of fthe iDrive WordPress backup plugin. This plugin is great in what it offers, which is free 2gb online automatic backup to iDrive's backup services for your entire site. However, the problem with JustHost.com is that the cron job associated with iDrive will spike above their 10% CPU usage restriction for an extended period of time. Which will result in your account received a very simple "Suspended" email.

Of course JustHost.com could try a couple things before total suspension, such as an email to the user prior to suspension, or maybe even terminating the cron job plus the email. However, I will say that they were very willing to work through the issue if you are aware of what probably caused the issue and sincerely want to fix it. Which was my case.

So for anyone using Justhost.com and wordpress, be sure you don't give iDrive Wordpress backup plugin a whirl.
