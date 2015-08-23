---
layout: page
status: publish
published: true
title: SDD
author:Jonathan
wordpress_id: 240
wordpress_url: http://www.jonathanhardison.com/?page_id=240
date: '2009-10-04 21:21:27 -0500'
date_gmt: '2009-10-05 03:21:27 -0500'
categories:
- Uncategorized
tags: []
comments: []
---
![MainICON]({{site.base}}/imagecontent/2009/10/MainICON21.bmp)

SharePoint Data Dump is an application designed to dump the binary contents of the Docs table back to their original format.
Useful for mass export, as well as recovery to file of a live or restored database.

For instance, you restore from backup to a temporary database and want to export all the files that were in a specific folder in SharePoint. You would simply give the application the server name and database name for the temporary database, and then enter the *directory/folder* name into the *Search LeafName* option. Supply a destination for exported files and click export.

![SDD Welcome Screen]({{site.base}}/imagecontent/2009/10/Capture1.PNG)

![SDD Settings Screen]({{site.base}}/imagecontent/2009/10/Capture2.PNG)

![SDD Filled Out Settings Screen]({{site.base}}/imagecontent/2009/10/Capture3.PNG)

![SDD Preview Table Screen]({{site.base}}/imagecontent/2009/10/Capture4.PNG)

![SDD Completed Export Message]({{site.base}}/imagecontent/2009/10/Capture5.PNG)

![SDD Updater Active With No Updates Available]({{site.base}}/imagecontent/2009/10/Capture6.PNG)

SDD v1.3 System Requirements:

  * Windows XP, Vista, 7, 2003, 2008
  * Microsoft .NET Framework 3.5
  * SharePoint 2007


Development of 1.5 continues, here is a nice screen shot showing the progression of the UI.

![SSDNewVersion]({{site.base}}/imagecontent/2009/10/Capture11.png)

Upcoming Changes:

  * Support for SharePoint 2010
  * Support for export to directory following leafname
  * Move export operations to a new thread.

#Download

Download the latest version [here](http://www.jonathanhardison.com/upload/SDD_v_1_1_3_1.msi){:target="_blank"}