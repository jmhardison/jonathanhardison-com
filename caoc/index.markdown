---
layout: page
status: publish
published: true
title: CAOC
author:Jonathan
author_login: jmhadmin
author_email: jmh@jonathanhardison.com
wordpress_id: 1210
wordpress_url: http://www.jonathanhardison.com/?page_id=1210
date: '2013-11-01 21:48:25 -0500'
date_gmt: '2013-11-02 03:48:25 -0500'
categories: []
tags: []
comments: []
---
#0.8.1.90 (05/31/2014) Released

##About

[CEX.io](https://cex.io/r/0/jhardison/0/){:target="_blank"} Auto Order Client is a quick little Windows program I'm working on that takes the grunt work of re-investing BTC profits back as GHS orders. The program carries the capability to log the order information, and keep a running persisted reserve balance if you set a reserve percentage. The reserve percentage takes a chunk of your profits out of the available balance that is used to purchase GHS. This amount compounds from order to order. If you set the percent to 0% you will not retain any, and all profits will be re-invested.

##Getting Started

To start, you will install the application via the installer. After the program and all pre-requsites are installed, you may launch the program by clicking on it in the Start Menu.
After launch, navigate to *settings* to apply specific information needed to begin auto orders.

![SettingsDialog]({{ site.base }}/imagecontent/2013/11/settingsdialog.png)

Several items are needed for this application to work.
  * The API Key and Secret are obtained by visiting your profile on Cex.io and configuring API access.
  * Username is the Cex.io username for your account.
  * Balance Check Interval is in seconds, should really not be lower than 60. This is how often the application will check for the balance. An item to remember is CEX.io will ban your IP if you access their API service more than 600 times in 10 minutes.
  * Divided into two sections, BTC and NMC both have their own independent configuration.

  * BTC / NMC Auto Order Enabled turns on the auto-reinvest for that currency.
  * Threshold is the amount of BTC or NMC available that you want to initiate an order at. Please note that if the resulting GHS amount that you can buy is less than .0001, the order will not be processed. (Cex.io minimum requirement.)
  * Reserve Percent is how much of your available balance minus any already reserved amount, that you want to keep back from the order.
  * The Clear Reserve button sets the reserved amount back to 0.

![APISetup]({{ site.base }}/imagecontent/2013/11/apisetup.png)

On Cex.io under your profile and API section, specify your public IP address the system running the application will be seen as, and tick all four permissions.
Click Generate Key and copy KEY and SECRET to the application settings, and then click the activate link to enable this key. At this time the secret will be masked on the site.

After you have entered all information into the settings dialog, click *OK* and the program will start its timer based on your definition. The balance and log is updated with your timer for orders, so you may or may not see anything immediately.
Once running, you can sit back and let the application do the grunt work for you.

![MainProgram]({{ site.base }}/imagecontent/2013/11/mainprogram.png)

##Known Issues

Some known issues with the application are:

  * BTC/GHS balances are sometimes wrong in the log. I changed up the method I was calculating the balance, but 8 decimal places are a whole lot of fun. But there is an issue with the API as well on orders that you can result in a negative balance. To prevent this I have standardized on both rounding down to the 8th decimal place as well as in cases of orders subtracting 0.00000002 from the available balance. This helps keep my tests above being a negative balance.
  * Occasionally there is a zero balance item in the log. Currently one of two things will occur when CEX.io is unreachable. One is the application appears to do nothing like normal or freeze, the other is a zero balance or blank entry in the log. I've tried to catch these and prevent them and my latest version might have this resolved. But none the less, it can occur.
  * There is occasional a display issue resulting in balances not showing correctly in the log. I plan to rework this and have the log balances derived from a post order balance check.
  * There is a known issue with CEX.io that results occasionally in incorrect balance display. This issues is being worked on, but does not impact your use of the service.
    
      > ![BalanceDisplayIssue]({{ site.base }}/imagecontent/2013/11/balancedisplayissue.png)

##Possible Enhancements

Some items I'm working on for the next version(s):

  * Adding a "refresh" button to the balance screen. (Would also cause a buy order if threshold is met.)
  * Adding a random "downward" pressure order that submits an order slightly under the lowest asking price.
  * Adding order followup. Some orders can be incomplete and have a remaining amount to purchase that hangs in the system. This would enhance the application to check in on orders and make sure they are "completed". This also ties into downward pressure, as the pending order would have to be tracked.

##Help Support The Project

If you care to donate in support of this application, you can send some loved BTC direct to the following wallet address, or by using this [link](https://coinbase.com/checkouts/8604b67e441f07513abd5c0d54328978){:target="_blank"}

  > ![Chart]({{ site.base }}/imagecontent/2013/11/chart.png)
  > 1LgUcP9k8kCVEfSxSsP8TKejMY9B8d1vAx

Any little bit would be appreciated and would help motivate future development. Or if you like you can send some CEX.io GHS Vouchers over to the support email. [caocsupport (at) lmdev (dot) net].

###No Wallet?

If you need an online wallet, you can get one [here](https://coinbase.com/?r=522e1c16f52347065300005e&utm_campaign=user-referral&src=referral-link){:target="_blank"}

##Still Not Signed Up For Cex.io?

If you don't have an account at CEX.io, click this pretty banner! Not sure what good my application will do for you if you are not signed up for their services...
[![CEX.io - Bitcoin Commodity Exchange](http://cex.io/img/b/728x90.jpg)](https://cex.io/r/0/jhardison/0/)

##Support or Obtaining Help

Please remember this is an alpha version and as such is going to carry some issues. If you have any issues or features you wish to send, you can submit an email to *caocsupport [at] lmdev [dot] net*

##Release Info

* 0.8.1.3
  * Initial alpha release to public.

* 0.8.1.26 (11/15/2013)
  * Resolved an issue with non en-US regions that do not use a period (.) as their decimal separator. This caused the application to appear to not function or make trades.
  * Added status indicators to show when the client purchase is enabled, as well as the last and next polling times.
  * Changed ClickOnce deployment options to derive from www.JonathanHardison.com.
  * Added "Check For Updates" feature to application.

* 0.8.1.32 (11/15/2013)
  * Resolved updater issue.
  * Added BTC Reserved Balance to status bar.

* 0.8.1.36 (11/16/2013)
  * Enhanced data grid display.
  * Resolved percentage rounding issue on settings dialog.
  * Added additional input validation on settings dialog.
  * Began cleanup and reorganization of settings dialog in prep for NMC.
  * Rebound and removed resize restriction on dialog.

* 0.8.1.49 (11/18/2013)
  * NMC re-invest support added.
  * NMC re-invest has a limit to only place orders for GHS >= .0001
  * Signing installer.

* 0.8.1.59 (12/05/2013)
  * Added logging tab.
  * Added error information capture to db, such as an error loading settings or object reference not set errors.
  * Added informational capture to db, such as resulting GHS order being below the minimum .0001 that is required.
  * Added logging tab export to csv.

* 0.8.1.71 (02/09/2014
  * Changed minimum order of GHS to .00000001 to help with ultra-low volume orders.
  * Added ability to clear tables individually. *Please note it could take several tries, I will add in the next version a lock on the timer while the clear is processing.*
  * Experimental currency conversion added. This feature will attempt to convert to the high yield currency for purchasing GHS. *Not stable, and could result in failed orders.*
  * Added capture of request/response JSON into DB. This will be exposed to the user in the GUI in a future version.
  * Resolved several issues causing "Error during poll worker: Input string was not in the correct format."

* 0.8.1.73 (03/10/2014)
  * Resolved some issues where reserved percentages were not being used correctly. For example a reservation of 10% or 50% in settings results in using 1% or 5% on polling actions.
  * Began work on splitting CAOC libraries into public releasable parts, while keeping the GUI elements that use licensed components closed.

* 0.8.1.90 (05/31/2014)
  * Added experimental IXC/LTC trading to BTC.
  * Added new settings tabs and grid tabs to handle trading of new alts.
  * Added more currencies to balance group box.
  * Added more error handling to catch the real response from CEX.io and log it, as opposed to "value cannot be null" errors.
  * Currency conversion is still experimental, and does have an issue when combined with alt trading. (Trade will stop when conversion fails for that round.)
  * Added CEX.io trade fee into calculating usable balance.

##Download Installer

The latest version of the downloader is available [here](http://www.jonathanhardison.com/caocdist/setup.exe){:target="_blank"}
