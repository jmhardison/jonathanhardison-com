---
layout: post
status: publish
published: true
title: XP&#47;2003 Delayed Start Service
author:
  display_name: Jonathan
  login: jmhadmin
  email: jmh@jonathanhardison.com
  url: ''
author_login: jmhadmin
author_email: jmh@jonathanhardison.com
wordpress_id: 492
wordpress_url: http://www.jonathanhardison.com/index.php/2010/04/30/xp2003-delayed-start-service/
date: '2010-04-30 14:33:15 -0500'
date_gmt: '2010-04-30 20:33:15 -0500'
categories:
- Uncategorized
tags: []
comments: []
---
<p>Man I haven't had to do this in a while since Vista and Windows 7 all have the Automatic (Delayed) start option for services. But in case you need to delay start a process on xp&#47;2003. Find the service in HKEY_LOCAL_MACHINESYSTEMCurrentControlSetServices<Service name></p>
<p>Add a new value (REG_MULTI_SZ) and call it "DependOnService" without quotes.<br />
Next put the value as the service you want to delay the start until after. The processes normally used are Spooler and Messenger.</p>
