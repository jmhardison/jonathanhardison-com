---
layout: page
status: publish
published: true
title: CAOC
author:
  display_name: Jonathan
  login: jmhadmin
  email: jmh@jonathanhardison.com
  url: ''
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
<h2><span style="color: #0000ff;">0.8.1.90 (05&#47;31&#47;2014) Released<&#47;span><&#47;h2></p>
<h1>About<&#47;h1><br />
<a title="CEX.io" href="https:&#47;&#47;cex.io&#47;r&#47;0&#47;jhardison&#47;0&#47;" target="_blank">Cex.io<&#47;a> Auto Order Client is a quick little Windows program I'm working on that takes the grunt work of re-investing BTC profits back as GHS orders. The program carries the capability to log the order information, and keep a running persisted reserve balance if you set a reserve percentage. The reserve percentage takes a chunk of your profits out of the available balance that is used to purchase GHS. This amount compounds from order to order. If you set the percent to 0% you will not retain any, and all profits will be re-invested.</p>
<h1>Getting Started<&#47;h1><br />
To start, you will install the application via the installer. After the program and all pre-requsites are installed, you may launch the program by clicking on it in the Start Menu.</p>
<p>After launch, navigate to <span style="text-decoration: underline;">settings<&#47;span> to apply specific information needed to begin auto orders.</p>
<p><a href="http:&#47;&#47;www.jonathanhardison.com&#47;wp-content&#47;uploads&#47;2013&#47;11&#47;settingsdialog.png"><img class="size-medium wp-image-1212 alignright" src="http:&#47;&#47;www.jonathanhardison.com&#47;wp-content&#47;uploads&#47;2013&#47;11&#47;settingsdialog.png" alt="settings" width="300" height="182" &#47;><&#47;a>Several items are needed for this application to work.</p>
<ul>
<li>The API Key and Secret are obtained by visiting your profile on Cex.io and configuring API access.<&#47;li>
<li>Username is the Cex.io username for your account.<&#47;li>
<li>Balance Check Interval is in seconds, should really not be lower than 60. This is how often the application will check for the balance. An item to remember is CEX.io will ban your IP if you access their API service more than 600 times in 10 minutes.<&#47;li>
<li>Divided into two sections, BTC and NMC both have their own independent configuration.
<ul>
<li>BTC&#47;NMC Auto Order Enabled turns on the auto-reinvest for that currency.<&#47;li>
<li>Threshold is the amount of BTC or NMC available that you want to initiate an order at. Please note that if the resulting GHS amount that you can buy is less than .0001, the order will not be processed. (Cex.io minimum requirement.)<&#47;li>
<li>Reserve Percent is how much of your available balance minus any already reserved amount, that you want to keep back from the order.<&#47;li>
<li>The Clear Reserve button sets the reserved amount back to 0.<&#47;li><br />
<&#47;ul><br />
<&#47;li><br />
<&#47;ul><br />
&nbsp;</p>
<p><a href="http:&#47;&#47;www.jonathanhardison.com&#47;wp-content&#47;uploads&#47;2013&#47;11&#47;apisetup.png"><img class="size-medium wp-image-1213 alignleft" src="http:&#47;&#47;www.jonathanhardison.com&#47;wp-content&#47;uploads&#47;2013&#47;11&#47;apisetup-300x120.png" alt="apisetup" width="300" height="120" &#47;><&#47;a></p>
<p>On Cex.io under your profile and API section, specify your public IP address the system running the application will be seen as, and tick all four permissions.</p>
<p>Click Generate Key and copy KEY and SECRET to the application settings, and then click the activate link to enable this key. At this time the secret will be masked on the site.</p>
<p>&nbsp;</p>
<p>After you have entered all information into the settings dialog, click <span style="text-decoration: underline;">OK<&#47;span> and the program will start its timer based on your definition. The balance and log is updated with your timer for orders, so you may or may not see anything immediately.</p>
<p>Once running, you can sit back and let the application do the grunt work for you.</p>
<p><a href="http:&#47;&#47;www.jonathanhardison.com&#47;wp-content&#47;uploads&#47;2013&#47;11&#47;mainprogram.png"><img class="alignnone size-medium wp-image-1214" src="http:&#47;&#47;www.jonathanhardison.com&#47;wp-content&#47;uploads&#47;2013&#47;11&#47;mainprogram.png" alt="appsdisplay" width="300" height="192" &#47;><&#47;a></p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<h1>Upgrades<&#47;h1><br />
The current upgrade method from 0.8.1.3 to any new version requires you backup your old DB files if you wish to persist them. Otherwise you can uninstall and install the new version fresh. To move to a newer version is treated as a new application install due to changes in the ClickOnce Deployment. Upgrades from the new edition further are handled within the application by clicking "Help" and the "Check For Updates".</p>
<p>To perform an upgrade from 0.8.1.3 to a new version please follow these steps if you wish to save your data.</p>
<ol>
<li>Navigate to the following path and backup the database files.c:\users\%username%\appdata\local\apps\2.0\data\And it is most likely in, but you will need to search around:<br />
\RGT0MRGD.WL6\4OGC61L1.YWN\cexa..tion_d807611235438430_0000.0008_232436946024a986\dataIf you do not have this location, search the paths under c:\users\%username%\appdata\local\apps\2.0\data\ and look for the files (CAOCDataCore.mdf and CAOCDataCore_log.ldf) and copy these to a new location.<&#47;li></p>
<li>Uninstall CAOC<&#47;li>
<li>Install the new version of CAOC from the site http:&#47;&#47;www.JonathanHardison.com&#47;index.php&#47;caoc<&#47;li>
<li>After install, close the program and navigate to the following path:<br />
c:\users\%username%\appdata\local\apps\2.0\data\And again drill into the path of \RGT0MRGD.WL6\4OGC61L1.YWN\cexa..tion_<long number string>\Data<br />
Paste the backed up DB files into this path.<&#47;li></p>
<li>Launch CAOC.<&#47;li><br />
<&#47;ol><br />
&nbsp;</p>
<p>Going from 0.8.1.32 to the latest also requires you to preserve your DB's, as outlined above. However you do not need to uninstall the old version first.</p>
<h1>Known Issues<&#47;h1><br />
Some known issues with the application are:</p>
<ul>
<li>BTC&#47;GHS balances are sometimes wrong in the log. I changed up the method I was calculating the balance, but 8 decimal places are a whole lot of fun. But there is an issue with the API as well on orders that you can result in a negative balance. To prevent this I have standardized on both rounding down to the 8th decimal place as well as in cases of orders subtracting 0.00000002 from the available balance. This helps keep my tests above being a negative balance.<&#47;li>
<li>Occasionally there is a zero balance item in the log. Currently one of two things will occur when CEX.io is unreachable. One is the application appears to do nothing like normal or freeze, the other is a zero balance or blank entry in the log. I've tried to catch these and prevent them and my latest version might have this resolved. But none the less, it can occur.<&#47;li>
<li>There is occasional a display issue resulting in balances not showing correctly in the log. I plan to rework this and have the log balances derived from a post order balance check.<&#47;li>
<li>There is a known issue with CEX.io that results occasionally in incorrect balance display. This issues is being worked on, but does not impact your use of the service.<a href="http:&#47;&#47;www.jonathanhardison.com&#47;wp-content&#47;uploads&#47;2013&#47;11&#47;balancedisplayissue.png"><img src="http:&#47;&#47;www.jonathanhardison.com&#47;wp-content&#47;uploads&#47;2013&#47;11&#47;balancedisplayissue-300x36.png" alt="balancedisplayissue" width="300" height="36" &#47;><&#47;a><&#47;li><br />
<&#47;ul><br />
&nbsp;</p>
<h1>Possible Enhancements<&#47;h1><br />
Some items I'm working on for the next version(s):</p>
<ul>
<li>Adding a "refresh" button to the balance screen. (Would also cause a buy order if threshold is met.)<&#47;li>
<li>Adding a random "downward" pressure order that submits an order slightly under the lowest asking price.<&#47;li>
<li>Adding order followup. Some orders can be incomplete and have a remaining amount to purchase that hangs in the system. This would enhance the application to check in on orders and make sure they are "completed". This also ties into downward pressure, as the pending order would have to be tracked.<&#47;li><br />
<&#47;ul><br />
&nbsp;</p>
<h1>Help Support The Project<&#47;h1><br />
If you care to donate in support of this application, you can send some loved BTC direct to the following wallet address, or by using this link (<a href="https:&#47;&#47;coinbase.com&#47;checkouts&#47;8604b67e441f07513abd5c0d54328978" target="_blank">Donate Bitcoins<&#47;a>):<br />
<img class="size-full wp-image-1219 alignleft" src="http:&#47;&#47;www.jonathanhardison.com&#47;wp-content&#47;uploads&#47;2013&#47;11&#47;chart.png" alt="chart" width="194" height="194" &#47;></p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>1LgUcP9k8kCVEfSxSsP8TKejMY9B8d1vAx</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>Any little bit would be appreciated and would help motivate future development. Or if you like you can send some CEX.io GHS Vouchers over to the support email. [caocsupport (at) lmdev (dot) net].</p>
<p>&nbsp;</p>
<h1>No Wallet?<&#47;h1><br />
If you need an online wallet, you can get one at <a href="https:&#47;&#47;coinbase.com&#47;?r=522e1c16f52347065300005e&amp;utm_campaign=user-referral&amp;src=referral-link">Coinbase<&#47;a>.</p>
<p>&nbsp;</p>
<h1>Still Not Signed Up For Cex.io?<&#47;h1><br />
If you don't have an account at CEX.io, click this pretty banner! Not sure what good my application will do for you if you are not signed up for their services...<br />
<a title="CEX.io - Bitcoin Commodity Exchange" href="https:&#47;&#47;cex.io&#47;r&#47;0&#47;jhardison&#47;0&#47;" target="_blank"><img src="http:&#47;&#47;cex.io&#47;img&#47;b&#47;728x90.jpg" alt="CEX.io" width="728" height="90" border="0" &#47;><&#47;a></p>
<p>&nbsp;</p>
<h1>Support or Obtaining Help<&#47;h1><br />
Please remember this is an alpha version and as such is going to carry some issues. If you have any issues or features you wish to send, you can submit an email to <strong>caocsupport [at] lmdev [dot] net<&#47;strong>.</p>
<p>&nbsp;</p>
<h1>Release Info<&#47;h1></p>
<ul>
<li>0.8.1.3
<ul>
<li>Initial alpha release to public.<&#47;li><br />
<&#47;ul><br />
<&#47;li></p>
<li>0.8.1.26 (11&#47;15&#47;2013)
<ul>
<li>Resolved an issue with non en-US regions that do not use a period (.) as their decimal separator. This caused the application to appear to not function or make trades.<&#47;li>
<li>Added status indicators to show when the client purchase is enabled, as well as the last and next polling times.<&#47;li>
<li>Changed ClickOnce deployment options to derive from www.JonathanHardison.com.<&#47;li>
<li>Added "Check For Updates" feature to application.<&#47;li><br />
<&#47;ul><br />
<&#47;li></p>
<li>0.8.1.32 (11&#47;15&#47;2013)
<ul>
<li>Resolved updater issue.<&#47;li>
<li>Added BTC Reserved Balance to status bar.<&#47;li><br />
<&#47;ul><br />
<&#47;li></p>
<li>0.8.1.36 (11&#47;16&#47;2013)
<ul>
<li>Enhanced data grid display.<&#47;li>
<li>Resolved percentage rounding issue on settings dialog.<&#47;li>
<li>Added additional input validation on settings dialog.<&#47;li>
<li>Began cleanup and reorganization of settings dialog in prep for NMC.<&#47;li>
<li>Rebound and removed resize restriction on dialog.<&#47;li><br />
<&#47;ul><br />
<&#47;li></p>
<li>0.8.1.49 (11&#47;18&#47;2013)
<ul>
<li>NMC re-invest support added.<&#47;li>
<li>NMC re-invest has a limit to only place orders for GHS >= .0001<&#47;li>
<li>Signing installer.<&#47;li><br />
<&#47;ul><br />
<&#47;li></p>
<li>0.8.1.59 (12&#47;05&#47;2013)
<ul>
<li>Added logging tab.<&#47;li>
<li>Added error information capture to db, such as an error loading settings or object reference not set errors.<&#47;li>
<li>Added informational capture to db, such as resulting GHS order being below the minimum .0001 that is required.<&#47;li>
<li>Added logging tab export to csv.<&#47;li><br />
<&#47;ul><br />
<&#47;li></p>
<li>0.8.1.71 (02&#47;09&#47;2014
<ul>
<li>Changed minimum order of GHS to .00000001 to help with ultra-low volume orders.<&#47;li>
<li>Added ability to clear tables individually. *Please note it could take several tries, I will add in the next version a lock on the timer while the clear is processing.*<&#47;li>
<li>Experimental currency conversion added. This feature will attempt to convert to the high yield currency for purchasing GHS. *Not stable, and could result in failed orders.*<&#47;li>
<li>Added capture of request&#47;response JSON into DB. This will be exposed to the user in the GUI in a future version.<&#47;li>
<li>Resolved several issues causing "Error during poll worker: Input string was not in the correct format."<&#47;li><br />
<&#47;ul><br />
<&#47;li></p>
<li>0.8.1.73 (03&#47;10&#47;2014)
<ul>
<li>Resolved some issues where reserved percentages were not being used correctly. For example a reservation of 10% or 50% in settings results in using 1% or 5% on polling actions.<&#47;li>
<li>Began work on splitting CAOC libraries into public releasable parts, while keeping the GUI elements that use licensed components closed.<&#47;li><br />
<&#47;ul><br />
<&#47;li></p>
<li>0.8.1.90 (05&#47;31&#47;2014)
<ul>
<li>Added experimental IXC&#47;LTC trading to BTC.<&#47;li>
<li>Added new settings tabs and grid tabs to handle trading of new alts.<&#47;li>
<li>Added more currencies to balance group box.<&#47;li>
<li>Added more error handling to catch the real response from CEX.io and log it, as opposed to "value cannot be null" errors.<&#47;li>
<li>Currency conversion is still experimental, and does have an issue when combined with alt trading. (Trade will stop when conversion fails for that round.)<&#47;li>
<li>Added CEX.io trade fee into calculating usable balance.<&#47;li><br />
<&#47;ul><br />
<&#47;li><br />
<&#47;ul></p>
<h1>Download Installer<&#47;h1><br />
[dm]17[&#47;dm]</p>
