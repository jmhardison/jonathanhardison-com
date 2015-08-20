---
layout: post
status: publish
published: true
title: Google Apps with ADFS Password Change Web App.
author:
  display_name: Jonathan
  login: jmhadmin
  email: jmh@jonathanhardison.com
  url: ''
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
<p>So I've been quiet now for a bit, but here is the story on what I've been working on lately. Recently I've been helping do a migration from Exchange to Google Apps using ADFS 2.0 as the SSO. Everything in regards to authentication is working, but to simply user support and provide the end user the ability to change their own "built in google apps user" without envolving IT or purchasing some expensive product... I have created my own.</p>
<p>It will authenticate the user against ADFS and then using the Google API will allow that user to change their Google Apps User password to one they define. This allows them to set&#47;reset their password that is used by non web requests such as IMAP, desktop software and mobile phones.</p>
<p>&nbsp;</p>
<h1><strong>UPDATE May 13th, 2011:<&#47;strong><&#47;h1><br />
I have continued work on this project and now at version 0.6.0 it is almost to a completed first render model of the application. New features I have added:</p>
<ul>
<li>History Per User&#47;Viewable by user.<&#47;li>
<li>PIN Code Creation with detection of missing PIN and forced creation.<&#47;li>
<li>Streamlined Menu, using DevExpress components.<&#47;li>
<li>Various performance enhancements and bug fixes.<&#47;li><br />
<&#47;ul></p>
<div><&#47;div><br />
Coming up next:</p>
<ul>
<li>Implement PIN Code Management.<&#47;li>
<li>Implement PIN Code&nbsp;usage&nbsp;in password change routine.<&#47;li>
<li>Implement PIN Code encryption routines.<&#47;li>
<li>Implement password complexity logic.<&#47;li>
<li>Implement PIN Code validation logic.<&#47;li><br />
<&#47;ul></p>
<div>I'm edging closer and closer to completion and hopefully soon I will be able to move to Dual Password Change URL for Google Apps SSO. The goal of that project is to provide a Password &nbsp;Change URL that you can use to allow the user to change both their AD password and the Google Apps user password at the same time.<&#47;div></p>
<div><&#47;div></p>
<h1><strong>Update June 3rd, 2011:<&#47;strong><&#47;h1></p>
<div><&#47;div></p>
<div>After another few weeks of being away, getting married and such, I'm back and have an update on the progress.<&#47;div></p>
<div>As above I had listed a few items coming up next, well here is what is now in this release:<&#47;div></p>
<div><&#47;div></p>
<div>
<ul>
<li>Implement PIN Code Management.<&#47;li>
<li>Implement PIN Code&nbsp;usage&nbsp;in password change routine.<&#47;li>
<li>Implement PIN Code encryption routines.<&#47;li>
<li>Implement password complexity logic.<&#47;li>
<li>Implement PIN Code validation logic.<&#47;li><br />
<&#47;ul></p>
<div>That's right, that whole list is in now. The password complexity logic is based on complexity requirements from Google to try to prevent any account from being hit by the Captcha response system.<&#47;div></p>
<div><&#47;div></p>
<div>Up next on my plate of goodness:<&#47;div></p>
<div><&#47;div></p>
<div>
<ul>
<li>Implement Management Application For Site. This will be a standalone application that ties into the database&nbsp;back-end.<&#47;li>
<li>Implement theming on the site that is nicer than what currently is in use.<&#47;li>
<li>Implement client side in page validation before delivery to server for validation.<&#47;li>
<li>Implement full&nbsp;sign-out&nbsp;and cleanup of ADFS cookies from management site.<&#47;li><br />
<&#47;ul><br />
<&#47;div><br />
<&#47;div></p>
