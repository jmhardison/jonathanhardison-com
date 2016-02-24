---
layout: post
title:  "Azure AD Licensing Woes?!"
date:   2016-02-23 21:04:42
categories: general
author: Jonathan
comments: true
share:
---
For anyone trying to acquire Azure AD Basic Licenses for a tenant other than your default corporate tenant within an Enterprise Agreement (think o365 here), you might just be out of luck.
In working with Microsoft we've figured out that effectively nobody within their organization fully understands how to both sell the licenses, as well as support them. Numerous premier cases and
discussions result in the resounding confirmation that those licenses are just not meant for anyone.

Under the covers, the issue is simply that licenses for Azure AD are assigned to an Agreement Number (AN). That AN is then assigned to a tenant in Azure AD. And here is the kicker... One AN cannot be
assigned or shared between tenants. But how do you get an AN? Well simple, you just have to go back through the license process... well not so simple. Getting those agreements set up is like an act of
congress. Not to mention, if you work for a company that has a legal department, you have just commited yourself to a fine dining experience with some lawyers. All to no avail... you see, my believe is that
Microsoft doesn't actually 'want' to sell these things. If they did, they wouldn't be one of the only components of Azure that do not work like a consumptive service. DevOps mentality shattering, 1990's style
ordering is it's preference. That's right, no button to purchase, but you can pick up the phone and call third party distributor! Taste's like modern, no?

So what do you do?! If you are wanting to use Azure AD as an auth store, maybe for a cloud application, what are you to do? 

Enter, Azure AD B2C... the thing that takes Azure AD, mucks with it's license setup and associates it to a subscription with duck tape and bailing wire.
I have this believe that before Azure AD changed ownership inside Microsoft that the original group thought up Basic Licensing, and the new group through up B2C. Just an observation from the outside world.
Seriously, why would we have a half baked product license for the old one that has no automated order process, replaced by a kind-of-new-kinda-old one that removes it and makes it consumptive?

Either way, both need some serious attention from the user experience department. Azure AD and Azure AD B2C both feel and act like an afterthought... a monster created by a mad scientist using spare body parts.

/Rant
