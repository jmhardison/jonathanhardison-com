---
layout: post
status: publish
published: true
title: ADFS 2.0 Claims Incomplete or Wrong on username change.
author:Jonathan
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
If you use AD FS 2.0, then you may have run across an issue before where after the username has been changed things do not come back correctly. This could be where you see fewer claims coming back and including the Windows Account Name shows the previous name. This is a because of caching performed by the LSA service, and as a result the old information gets used. Changing a persons account name is not uncommon, such as a person changing their name for marriage, so this fix should keep you running in those cases.


To correct this you have a couple choices... first up is you can reboot the server to clear the LSA cache. Or you can do the following, which I finally found as an option.

[Link](http://support.microsoft.com/default.aspx?scid=kb%3bEN-US%3b946358){:target="_blank"}
By changing the maximum cache size to 0, you effectively shut off the ability for LSA to cache requests. The best part of this change is that not only do you not have to reboot to clear the LSA cache, but you also do not have to reboot to implement the restriction of 0. It is an immediate change to the system.

To work around this issue, disable the local SID cache on the domain member computer. To do this, follow these steps:

  * Open Registry Editor.
  * Locate and then right-click the following registry subkey:
    * HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Lsa
  * Point to <strong>New</strong>, and then click DWORD Value.
  * Type LsaLookupCacheMaxSize, and then press ENTER.
  * Right-click LsaLookupCacheMaxSize, and then click Modify.
  * In the Value data box, type 0, and then click OK.
  * Exit Registry Editor.

*Note* The LsaLookupCacheMaxSize registry entry sets the maximum number of cached mappings that can be saved in the local SID cache. The default maximum number is 128. When the LsaLookupCacheMaxSize registry entry is set to 0, the local SID cache is disabled.
