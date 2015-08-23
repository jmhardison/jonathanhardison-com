---
layout: post
status: publish
published: true
title: Google Apps with ADFS Password Change Web App.
author:Jonathan
author_login: jmhadmin
author_email: jmh@jonathanhardison.com
wordpress_id: 612
wordpress_url: http://www.jonathanhardison.com/?p=612
date: '2011-05-06 23:30:16 -0500'
date_gmt: '2011-05-07 05:30:16 -0500'
categories:
- Windows
- Internet
tags:
- LinkedIn
comments: []
---
So I've been quiet now for a bit, but here is the story on what I've been working on lately. Recently I've been helping do a migration from Exchange to Google Apps using ADFS 2.0 as the SSO. Everything in regards to authentication is working, but to simply user support and provide the end user the ability to change their own "built in google apps user" without envolving IT or purchasing some expensive product... I have created my own.

It will authenticate the user against ADFS and then using the Google API will allow that user to change their Google Apps User password to one they define. This allows them to set/reset their password that is used by non web requests such as IMAP, desktop software and mobile phones.

UPDATE May 13th, 2011:
I have continued work on this project and now at version 0.6.0 it is almost to a completed first render model of the application. New features I have added:

  * History Per User/Viewable by user.
  * PIN Code Creation with detection of missing PIN and forced creation.
  * Streamlined Menu, using DevExpress components.
  * Various performance enhancements and bug fixes.


Coming up next:

  * Implement PIN Code Management.
  * Implement PIN Code usage in password change routine.
  * Implement PIN Code encryption routines.
  * Implement password complexity logic.
  * Implement PIN Code validation logic.

I'm edging closer and closer to completion and hopefully soon I will be able to move to Dual Password Change URL for Google Apps SSO. The goal of that project is to provide a Password  Change URL that you can use to allow the user to change both their AD password and the Google Apps user password at the same time.

Update June 3rd, 2011:

After another few weeks of being away, getting married and such, I'm back and have an update on the progress.
As above I had listed a few items coming up next, well here is what is now in this release:

  * Implement PIN Code Management.
  * Implement PIN Code usage in password change routine.
  * Implement PIN Code encryption routines.
  * Implement password complexity logic.
  * Implement PIN Code validation logic.

That's right, that whole list is in now. The password complexity logic is based on complexity requirements from Google to try to prevent any account from being hit by the Captcha response system.

Up next on my plate of goodness:

  * Implement Management Application For Site. This will be a standalone application that ties into the database back-end.
  * Implement theming on the site that is nicer than what currently is in use.
  * Implement client side in page validation before delivery to server for validation.
  * Implement full sign-out and cleanup of ADFS cookies from management site.
