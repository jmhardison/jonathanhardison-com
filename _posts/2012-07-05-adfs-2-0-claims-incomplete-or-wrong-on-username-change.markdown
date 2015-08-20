---
layout: post
status: publish
published: true
title: ADFS 2.0 Claims Incomplete or Wrong on username change.
author:
  display_name: Jonathan
  login: jmhadmin
  email: jmh@jonathanhardison.com
  url: ''
author_login: jmhadmin
author_email: jmh@jonathanhardison.com
wordpress_id: 1137
wordpress_url: http://www.jonathanhardison.com/?p=1137
date: '2012-07-05 18:29:19 -0500'
date_gmt: '2012-07-06 00:29:19 -0500'
categories:
- Uncategorized
tags: []
comments: []
---
<p>If you use AD FS 2.0, then you may have run across an issue before where after the username has been changed things do not come back correctly. This could be where you see fewer claims coming back and including the Windows Account Name shows the previous name. This is a because of caching performed by the LSA service, and as a result the old information gets used. Changing a persons account name is not uncommon, such as a person changing their name for marriage, so this fix should keep you running in those cases.</p>
<p>&nbsp;</p>
<p>To correct this you have a couple choices&hellip; first up is you can reboot the server to clear the LSA cache. Or you can do the following, which I finally found as an option.</p>
<p><a tabindex="-1" href="http:&#47;&#47;support.microsoft.com&#47;default.aspx?scid=kb%3bEN-US%3b946358" target="_parent">http:&#47;&#47;support.microsoft.com&#47;default.aspx?scid=kb;EN-US;946358<&#47;a></p>
<p>&nbsp;</p>
<p>By changing the maximum cache size to 0, you effectively shut off the ability for LSA to cache requests. The best part of this change is that not only do you not have to reboot to clear the LSA cache, but you also do not have to reboot to implement the restriction of 0. It is an immediate change to the system.</p>
<p>&nbsp;</p>
<p>To work around this issue, disable the local SID cache on the domain member computer. To do this, follow these steps:</p>
<blockquote>
<ol start="1">
<li>Open Registry Editor.<br />
To do this in Windows XP or in Windows Server 2003, click <strong>Start<&#47;strong>, click <strong> Run<&#47;strong>, type regedit, and then click <strong>OK<&#47;strong>.<br />
To do this in Windows Vista and newer, Click&nbsp;<strong>Start<&#47;strong>, type regedit in the <strong> Start Search<&#47;strong> box, and then press ENTER.<&#47;li></p>
<li>Locate and then right-click the following registry subkey:<&#47;li><br />
<&#47;ol><br />
<strong>HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Lsa<&#47;strong></p>
<ol start="3">
<li>Point to <strong>New<&#47;strong>, and then click <strong>DWORD Value<&#47;strong>.<&#47;li>
<li>Type LsaLookupCacheMaxSize, and then press ENTER.<&#47;li>
<li>Right-click <strong>LsaLookupCacheMaxSize<&#47;strong>, and then click <strong>Modify<&#47;strong>.<&#47;li>
<li>In the <strong>Value data<&#47;strong> box, type 0, and then click <strong>OK<&#47;strong>.<&#47;li>
<li>Exit Registry Editor.<&#47;li><br />
<&#47;ol><br />
<strong>Note<&#47;strong> The LsaLookupCacheMaxSize registry entry sets the maximum number of cached mappings that can be saved in the local SID cache. The default maximum number is 128. When the LsaLookupCacheMaxSize registry entry is set to 0, the local SID cache is disabled.<&#47;blockquote></p>
