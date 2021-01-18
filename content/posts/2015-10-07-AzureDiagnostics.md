---
author: Jonathan
categories:
  - general
comments: true
date: 2015-10-07 09:04:42
share: null
title: Azure Adds Boot Diagnostics!
---

One of the issues that has existed with Azure as a cloud service provider was the simple lack of any access to the console. While it is understood the need for that access is rare, it is a valuable
diagnostic tool for when the state of your system falls on its face. Other cloud providers give access to the console not only for diagnostic processes, but also for operational use. But Azure has
been left in the corner. That is until now!

![BootDiag](/images/2015/10/snip_20151007091513.png)

Microsoft has enhanced Azure to allow for "boot diagnostics" which gives the tenant user the ability to see one of two things.

  * If running linux, the serial output stream is collected and displayed.
	![LinuxBoot](/images/2015/10/snip_20151007092803.png)
  * If running windows, the console screen is captured and displayed.
	![WindowsBoot](/images/2015/10/snip_20151007092828.png)

This is not a perfect offering, in that it is only "view" access to the consoles. It is, however, a great step forward from what we used to have access to.

So how does one actually start using this offering? It's quite simple, but it does require a configuration change to any VM that you want to enable the functionality on.

  * You can start by simply going into the [Azure Preview Portal](http://portal.azure.com){:target="_blank"}.
  * After you sign in, navigate to a VM you want to enable functionality on.
  * If you have not enable diagnostics on this VM, you will be required to do that. Navigate to "Diagnostics" and enable it, giving it a storage account, and selecting the diag options you want before clicking save.
	![NoBootDiag](/images/2015/10/snip_20151007092029.png)
	* You can actually complete enabling the diagnostics and boot diagnostics in this one step. Just be sure you select "boot diagnostics".
		![EnableBootDiag](/images/2015/10/snip_20151007092045.png)
  * If you have enabled diagnostics already o this VM, you can go into "Diagnostics" and tick "Boot Diagnostics" to enable that functionality. If you go into "Boot Diagnostics" without it enabled, it will allow you to enable it as well.

Pretty simple... Now reboot your VM and you should start to receive collected information in the "Boot Diagnostics" screen.