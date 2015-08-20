---
layout: page
status: publish
published: true
title: WME
author:
  display_name: ''
  login: ''
  email: ''
  url: ''
wordpress_id: 170
wordpress_url: http://www.jonathanhardison.com/?page_id=170
date: '2009-04-08 08:07:42 -0500'
date_gmt: '2009-04-08 14:07:42 -0500'
categories:
- Uncategorized
tags: []
comments: []
---
<p><img class="alignnone size-full wp-image-176" style="border: 0px;" title="wmeicon" src="http:&#47;&#47;www.jonathanhardison.com&#47;wp-content&#47;uploads&#47;2009&#47;04&#47;wmeicon.png" alt="wmeicon" width="128" height="128" &#47;><a href="http:&#47;&#47;www.jonathanhardison.com&#47;wp-content&#47;uploads&#47;2009&#47;04&#47;2009-04-08_0020.png"><&#47;a>&nbsp;</p>
<p>WAV Marker Extractor is a program I threw together to export tracks from a single wave file that are designated by track markers.&nbsp;</p>
<p><a href="http:&#47;&#47;www.jonathanhardison.com&#47;wp-content&#47;uploads&#47;2009&#47;04&#47;2009-04-08_0020.png"><img class="alignnone size-medium wp-image-171" style="border: 0px;" title="WME Alpha APR2009" src="http:&#47;&#47;www.jonathanhardison.com&#47;wp-content&#47;uploads&#47;2009&#47;04&#47;2009-04-08_0020-300x187.png" alt="WME Alpha APR2009" width="300" height="187" &#47;><&#47;a>&nbsp;</p>
<p>I was involved in an audio project where the digitizers delivered around 1000 large wave files with track markers. My problem is I needed them exported with the track name as a searchable field (such as in metadata, or stuck into the resulting file name) with the addition of the artist name (which happened to be the first section of the source file name).&nbsp;</p>
<p>The result was WME. With WME I can feed it the source directory, and a destination directory. It will then enumerate the directory contents for all audio files and detect the track markers and place it in the table for you. Then you may export them all to their own wave files in a single batch process.&nbsp;</p>
<p>To convert to MP3, you need to obtain lame.exe and place into the install directory.&nbsp;</p>
<p><strong>Currently In Development (13APR2010):<&#47;strong>&nbsp;</p>
<ul>
<li>Rewrite of application from ground up in Visual Studio 2010 using .NET 4.0.<&#47;li>
<li>Main application will be designed around WPF, possibly allowing custom themes.<&#47;li>
<li>All functions that perform heavy work on database or audio files are being moved to a new class library.<&#47;li>
<li>All functions that perform heavy work will be written to support Parallel FX.<&#47;li>
<li>Application state saving will allow for you to save and load your progress across multiple uses of the application.<&#47;li>
<li>Log is being designed as part of the dataset handling all of the systems behind the scenes data.<&#47;li>
<li>Log will be exportable to file, allowing archival of any issues you have experienced.<&#47;li>
<li>Preview screen is being added to allow for modifications to file or track attributes prior to export. You will be able to modify any text that will wind up influencing the naming or metadata of the file once export is completed.<&#47;li>
<li>And more...<&#47;li><br />
<&#47;ul><br />
&nbsp;</p>
<p>[caption id="attachment_446" align="alignnone" width="300" caption="IDE screenshot of WME development.The file view shows all scanned files from the source path."]<a href="http:&#47;&#47;www.jonathanhardison.com&#47;wp-content&#47;uploads&#47;2009&#47;04&#47;Capture.png"><img class="size-medium wp-image-446 " style="border: 0px initial initial;" title="Capture" src="http:&#47;&#47;www.jonathanhardison.com&#47;wp-content&#47;uploads&#47;2009&#47;04&#47;Capture-300x121.png" alt="" width="300" height="121" &#47;><&#47;a>[&#47;caption]</p>
<div class="mceTemp">
<p>[caption id="attachment_468" align="alignnone" width="300" caption="The file view shows all scanned files from the source path."]<a href="http:&#47;&#47;www.jonathanhardison.com&#47;wp-content&#47;uploads&#47;2009&#47;04&#47;fileview.png"><img class="size-medium wp-image-468" title="FileView" src="http:&#47;&#47;www.jonathanhardison.com&#47;wp-content&#47;uploads&#47;2009&#47;04&#47;fileview-300x140.png" alt="" width="300" height="140" &#47;><&#47;a>[&#47;caption]</p>
<p>[caption id="attachment_469" align="alignnone" width="300" caption="Track view shows all detected tracks from the files in the source directory. The tracks and files are shown apart for ease, and then a final view will be the end result of the naming for the files."]<a href="http:&#47;&#47;www.jonathanhardison.com&#47;wp-content&#47;uploads&#47;2009&#47;04&#47;trackview.png"><img class="size-medium wp-image-469" title="Track View" src="http:&#47;&#47;www.jonathanhardison.com&#47;wp-content&#47;uploads&#47;2009&#47;04&#47;trackview-300x139.png" alt="Track view shows all detected tracks from the files in the source directory. The tracks and files are shown apart for ease, and then a final view will be the end result of the naming for the files." width="300" height="139" &#47;><&#47;a>[&#47;caption]</p>
<p><&#47;div><br />
&nbsp;</p>
<p><strong>19FEB2010 Changes:<&#47;strong>&nbsp;</p>
<ul>
<li>Changed compiler to x86 and reverted FMOD dll to 32bit version. This will allow the application to run on both systems.<&#47;li><br />
<&#47;ul><br />
<strong>18FEB2010 Changes:<&#47;strong>&nbsp;</p>
<ul>
<li>Fixed some error handling for long file names.<&#47;li>
<li>Added support for user installed lame.exe into install directory for MP3 conversion.<&#47;li>
<li>Added metadata support for MP3 conversions. Track Number, Track Name, Author and Album are filled out.<&#47;li><br />
<&#47;ul><br />
<strong>30DEC2009 Changes:<&#47;strong>&nbsp;</p>
<ul>
<li>Removed .Net 4.0 support and ParallelFX as it caused issues during export operation. Memory usage was too high for tested files.<&#47;li>
<li>Added base for excel file load to database. Providing the ability to map track name and artist values to more precise information from an excel sheet. Search right now will be by as much information I have derived from the file name to locate in the excel sheet. Currently the only requirement is that row 1 of the sheet is used as the columns row.<&#47;li>
<li>Ability to clean illegal filename characters from destination filename.<&#47;li>
<li>Ability to append chapter position in the destination filename. (Ie, marker 2 for lilo.wave becomes 2 - lilo.wave)<&#47;li>
<li>Replaced Updater application with new 1.0.2.x updater, providing support for msi based installers.<&#47;li>
<li>Removed redundant binding sources, and linked direct to dataset.<&#47;li><br />
<&#47;ul><br />
<strong>07SEP2009&nbsp;Changes:<&#47;strong>&nbsp;</p>
<ul>
<li>Currently testing in .Net 4.0 for ParallelFX support.<&#47;li>
<li>Added x64 compatability.<&#47;li>
<li>Added Auto-Update feature that pulls updates from master site.<&#47;li>
<li>Added ability to prepend track number to file name. Usefull in scenarios where there could be multiple "Song Intro" titles.<&#47;li>
<li>Created base installer for application.<&#47;li><br />
<&#47;ul><br />
[dm]10[&#47;dm]&nbsp;</p>
<p>[paypal-donation]</p>
