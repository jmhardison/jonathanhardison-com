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
<p><a href="http:&#47;&#47;www.jonathanhardison.com&#47;wp-content&#47;uploads&#47;2009&#47;10&#47;Capture10.png"><img style="border-bottom: 0px; border-left: 0px; display: inline; margin-left: 0px; border-top: 0px; margin-right: 0px; border-right: 0px" title="Capture" border="0" alt="Capture" align="left" src="http:&#47;&#47;www.jonathanhardison.com&#47;wp-content&#47;uploads&#47;2009&#47;10&#47;Capture_thumb3.png" width="240" height="259" &#47;><&#47;a>So I&rsquo;m toying with an auto update feature that I will embed into the little apps I write. Currently I&rsquo;m testing out how to detect forced manual updates and full local installers, as opposed to just a quick file patch. But in the process I found that I need to advertise myself for elevated privileges with UAC to perform updates on Windows 7. So the code to do this can be found over <a href="http:&#47;&#47;www.aneef.net&#47;2009&#47;06&#47;29&#47;request-uac-elevation-for-net-application-managed-code&#47;" target="_blank">here<&#47;a>! Basically you are modifying your applications manifest, and then checking the level in the app through a function to ensure you have it.<&#47;p></p>
