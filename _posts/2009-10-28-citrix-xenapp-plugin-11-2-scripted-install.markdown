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
<p>I had to revisit an old installer I had made that relied on a script running in the background for some additional software to be installed. This script also did a little cleanup of shortcuts, etc. I have since changed it all to run in InstallScript, however, this particular visit I didn&rsquo;t want to change it over to the new install. My problem is the installer for Citrix has gone through a drastic change. But never fear, the command line is super simple.</p>
<p>CitrixOnlinePluginFull.exe &#47;silent ADDLOCAL=&rdquo;ICA_Client,SSON,Flash,USB,DesktopViewer&rdquo;</p>
<p>Now you also need to know that PN.exe is officially gone in this release, so if you need the functions of that program, you can get the Citrix Quick Connect Tool to perform the same functions. But in a more RDP style screen.</p>
<p><a href="http:&#47;&#47;www.jonathanhardison.com&#47;wp-content&#47;uploads&#47;2009&#47;10&#47;Capture8.png"><img style="display: inline; border: 0px;" title="Capture" src="http:&#47;&#47;www.jonathanhardison.com&#47;wp-content&#47;uploads&#47;2009&#47;10&#47;Capture_thumb2.png" border="0" alt="Capture" width="240" height="121" &#47;><&#47;a></p>
<p><a href="http:&#47;&#47;www.jonathanhardison.com&#47;wp-content&#47;uploads&#47;2009&#47;10&#47;Capture9.png"><img style="display: inline; border: 0px;" title="Capture9" src="http:&#47;&#47;www.jonathanhardison.com&#47;wp-content&#47;uploads&#47;2009&#47;10&#47;Capture9_thumb.png" border="0" alt="Capture9" width="240" height="229" &#47;><&#47;a></p>
<p>Download the Quick Launch from <a href="http:&#47;&#47;support.citrix.com&#47;article&#47;CTX122536" target="_blank">here.<&#47;a></p>
