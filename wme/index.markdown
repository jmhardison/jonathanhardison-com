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
![WMEIcon]({{site.base}}/imagecontent/2009/04/wmeicon.png)

![WMEScreen]({{site.base}}/imagecontent/2009/04/2009-04-08_0020.png)

WAV Marker Extractor is a program I threw together to export tracks from a single wave file that are designated by track markers.

![WMEScreen2]({{site.base}}/imagecontent/2009/04/2009-04-08_0020.png)

I was involved in an audio project where the digitizers delivered around 1000 large wave files with track markers. My problem is I needed them exported with the track name as a searchable field (such as in metadata, or stuck into the resulting file name) with the addition of the artist name (which happened to be the first section of the source file name).

The result was WME. With WME I can feed it the source directory, and a destination directory. It will then enumerate the directory contents for all audio files and detect the track markers and place it in the table for you. Then you may export them all to their own wave files in a single batch process.

To convert to MP3, you need to obtain lame.exe and place into the install directory.

Currently In Development (13APR2010):

  * Rewrite of application from ground up in Visual Studio 2010 using .NET 4.0.
  * Main application will be designed around WPF, possibly allowing custom themes.
  * All functions that perform heavy work on database or audio files are being moved to a new class library.
  * All functions that perform heavy work will be written to support Parallel FX.
  * Application state saving will allow for you to save and load your progress across multiple uses of the application.
  * Log is being designed as part of the dataset handling all of the systems behind the scenes data.
  * Log will be exportable to file, allowing archival of any issues you have experienced.
  * Preview screen is being added to allow for modifications to file or track attributes prior to export. You will be able to modify any text that will wind up influencing the naming or metadata of the file once export is completed.
  * And more...

  > IDE screenshot of WME development.The file view shows all scanned files from the source path.
  > ![CaptureNew]({{site.base}}/imagecontent/2009/04/Capture.png)
  > ![FileView]({{site.base}}/imagecontent/2009/04/fileview.png)
  > Track view shows all detected tracks from the files in the source directory. The tracks and files are shown apart for ease, and then a final view will be the end result of the naming for the files.
  > ![trackview]({{site.base}}/imagecontent/2009/04/trackview.png)
  

19FEB2010 Changes:

  * Changed compiler to x86 and reverted FMOD dll to 32bit version. This will allow the application to run on both systems.

18FEB2010 Changes:

  * Fixed some error handling for long file names.
  * Added support for user installed lame.exe into install directory for MP3 conversion.
  * Added metadata support for MP3 conversions. Track Number, Track Name, Author and Album are filled out.

30DEC2009 Changes:

  * Removed .Net 4.0 support and ParallelFX as it caused issues during export operation. Memory usage was too high for tested files.
  * Added base for excel file load to database. Providing the ability to map track name and artist values to more precise information from an excel sheet. Search right now will be by as much information I have derived from the file name to locate in the excel sheet. Currently the only requirement is that row 1 of the sheet is used as the columns row.
  * Ability to clean illegal filename characters from destination filename.
  * Ability to append chapter position in the destination filename. (Ie, marker 2 for lilo.wave becomes 2 - lilo.wave)
  * Replaced Updater application with new 1.0.2.x updater, providing support for msi based installers.
  * Removed redundant binding sources, and linked direct to dataset.

07SEP2009 Changes:

  * Currently testing in .Net 4.0 for ParallelFX support.
  * Added x64 compatability.
  * Added Auto-Update feature that pulls updates from master site.
  * Added ability to prepend track number to file name. Usefull in scenarios where there could be multiple "Song Intro" titles.
  * Created base installer for application.

#Download

Download the latest version [here](http://www.jonathanhardison.com/upload/WME Setup.msi){:target="_blank"}
