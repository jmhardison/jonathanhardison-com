---
layout: post
status: publish
published: true
title: CardView Xceed DataGrid WPF Style!
author:
  display_name: Jonathan
  login: jmhadmin
  email: jmh@jonathanhardison.com
  url: ''
author_login: jmhadmin
author_email: jmh@jonathanhardison.com
wordpress_id: 193
wordpress_url: http://www.jonathanhardison.com/?p=193
date: '2009-05-22 21:19:15 -0500'
date_gmt: '2009-05-23 03:19:15 -0500'
categories:
- Uncategorized
tags:
- LinkedIn
comments: []
---
<p>So I took a quick break from all the installer creations I've been doing lately to enjoy some work on an old project... DCTracker!</p>
<p>I know, it is the neverending project, but when you get little time to work on anything else... blah blah. Ok, so here's the deal, I wanted to take my Child Attendance program from this:</p>
<p><a href="http:&#47;&#47;www.jonathanhardison.com&#47;wp-content&#47;uploads&#47;2009&#47;05&#47;captureold.jpg"><img class="alignnone size-medium wp-image-194" style="border: 0px;" title="Old child listing." src="http:&#47;&#47;www.jonathanhardison.com&#47;wp-content&#47;uploads&#47;2009&#47;05&#47;captureold-300x142.jpg" alt="Old child listing." width="300" height="142" &#47;><&#47;a></p>
<p>To this:</p>
<p><a href="http:&#47;&#47;www.jonathanhardison.com&#47;wp-content&#47;uploads&#47;2009&#47;05&#47;capturenew.jpg"><img class="alignnone size-medium wp-image-195" style="border: 0px;" title="New child listing." src="http:&#47;&#47;www.jonathanhardison.com&#47;wp-content&#47;uploads&#47;2009&#47;05&#47;capturenew-300x142.jpg" alt="New child listing." width="300" height="142" &#47;><&#47;a></p>
<p>Well wouldn't you know it, that is just super simple in Xceed DataGrid. (<a href="http:&#47;&#47;www.xceed.com">www.xceed.com<&#47;a>)</p>
<p>In the XAML of my window, I clicked "Show Configuration Window" on my datagrid.</p>
<p>Then selected cardview:</p>
<p><a href="http:&#47;&#47;www.jonathanhardison.com&#47;wp-content&#47;uploads&#47;2009&#47;05&#47;capturecardviewconfig1.jpg"><img class="alignnone size-medium wp-image-196" title="capturecardviewconfig1" src="http:&#47;&#47;www.jonathanhardison.com&#47;wp-content&#47;uploads&#47;2009&#47;05&#47;capturecardviewconfig1-300x222.jpg" alt="capturecardviewconfig1" width="300" height="222" &#47;><&#47;a></p>
<p>After selecting cardview and the theme I desired, I switched to the columns tab and setup my fields.</p>
<p><a href="http:&#47;&#47;www.jonathanhardison.com&#47;wp-content&#47;uploads&#47;2009&#47;05&#47;capturecolumns.jpg"><img class="alignnone size-medium wp-image-197" title="capturecolumns" src="http:&#47;&#47;www.jonathanhardison.com&#47;wp-content&#47;uploads&#47;2009&#47;05&#47;capturecolumns-300x224.jpg" alt="capturecolumns" width="300" height="224" &#47;><&#47;a></p>
<p>The "Field Name" corresponds to the field name in my dataset I will be passing, whereas "Title" is shown on the card.<br />
Next, we configure the data source in our code:</p>
<p><span style="color: #888888;"> <&#47;span></p>
<ol>
<li><span style="color: #339966;"><em>dataGridControlChildDisplay.ItemsSource = childListView;<&#47;em><&#47;span><&#47;li><br />
<&#47;ol><br />
chidlListView is an Observable Collection of my class:</p>
<pre lang="C#"><em><span style="color: #0000ff; font-size: x-small;"><span style="color: #0000ff; font-size: x-small;">public<&#47;span><&#47;span><span style="font-size: x-small;"> <&#47;span><span style="color: #0000ff; font-size: x-small;"><span style="color: #0000ff; font-size: x-small;">class<&#47;span><&#47;span><span style="font-size: x-small;"> <&#47;span><span style="color: #2b91af; font-size: x-small;"><span style="color: #2b91af; font-size: x-small;">attendanceListView<&#47;span><&#47;span><&#47;em><br />
<em>{<&#47;em><br />
<em><span style="color: #0000ff; font-size: x-small;"><span style="color: #0000ff; font-size: x-small;"> public<&#47;span><&#47;span><span style="font-size: x-small;"> <&#47;span><span style="color: #0000ff; font-size: x-small;"><span style="color: #0000ff; font-size: x-small;">bool<&#47;span><&#47;span><span style="font-size: x-small;"> isSelected { <&#47;span><span style="color: #0000ff; font-size: x-small;"><span style="color: #0000ff; font-size: x-small;">get<&#47;span><&#47;span><span style="font-size: x-small;">; <&#47;span><span style="color: #0000ff; font-size: x-small;"><span style="color: #0000ff; font-size: x-small;">set<&#47;span><&#47;span><span style="font-size: x-small;">; }<&#47;span><&#47;em><br />
<em><span style="color: #0000ff; font-size: x-small;"><span style="color: #0000ff; font-size: x-small;"> public<&#47;span><&#47;span><span style="font-size: x-small;"> <&#47;span><span style="color: #0000ff; font-size: x-small;"><span style="color: #0000ff; font-size: x-small;">string<&#47;span><&#47;span><span style="font-size: x-small;"> firstName { <&#47;span><span style="color: #0000ff; font-size: x-small;"><span style="color: #0000ff; font-size: x-small;">get<&#47;span><&#47;span><span style="font-size: x-small;">; <&#47;span><span style="color: #0000ff; font-size: x-small;"><span style="color: #0000ff; font-size: x-small;">set<&#47;span><&#47;span><span style="font-size: x-small;">; }<&#47;span><&#47;em><br />
<em><span style="color: #0000ff; font-size: x-small;"><span style="color: #0000ff; font-size: x-small;"> public<&#47;span><&#47;span><span style="font-size: x-small;"> <&#47;span><span style="color: #0000ff; font-size: x-small;"><span style="color: #0000ff; font-size: x-small;">string<&#47;span><&#47;span><span style="font-size: x-small;"> lastName { <&#47;span><span style="color: #0000ff; font-size: x-small;"><span style="color: #0000ff; font-size: x-small;">get<&#47;span><&#47;span><span style="font-size: x-small;">; <&#47;span><span style="color: #0000ff; font-size: x-small;"><span style="color: #0000ff; font-size: x-small;">set<&#47;span><&#47;span><span style="font-size: x-small;">; }<&#47;span><&#47;em><br />
<em><span style="color: #0000ff; font-size: x-small;"><span style="color: #0000ff; font-size: x-small;"> public<&#47;span><&#47;span><span style="font-size: x-small;"> <&#47;span><span style="color: #0000ff; font-size: x-small;"><span style="color: #0000ff; font-size: x-small;">string<&#47;span><&#47;span><span style="font-size: x-small;"> status { <&#47;span><span style="color: #0000ff; font-size: x-small;"><span style="color: #0000ff; font-size: x-small;">get<&#47;span><&#47;span><span style="font-size: x-small;">; <&#47;span><span style="color: #0000ff; font-size: x-small;"><span style="color: #0000ff; font-size: x-small;">set<&#47;span><&#47;span><span style="font-size: x-small;">; }<&#47;span><&#47;em><br />
<em><span style="color: #0000ff; font-size: x-small;"><span style="color: #0000ff; font-size: x-small;"> public<&#47;span><&#47;span><span style="font-size: x-small;"> <&#47;span><span style="color: #0000ff; font-size: x-small;"><span style="color: #0000ff; font-size: x-small;">string<&#47;span><&#47;span><span style="font-size: x-small;"> oldstatus { <&#47;span><span style="color: #0000ff; font-size: x-small;"><span style="color: #0000ff; font-size: x-small;">get<&#47;span><&#47;span><span style="font-size: x-small;">; <&#47;span><span style="color: #0000ff; font-size: x-small;"><span style="color: #0000ff; font-size: x-small;">set<&#47;span><&#47;span><span style="font-size: x-small;">; }<&#47;span><&#47;em><br />
<em><span style="color: #0000ff; font-size: x-small;"><span style="color: #0000ff; font-size: x-small;"> public<&#47;span><&#47;span><span style="font-size: x-small;"> <&#47;span><span style="color: #0000ff; font-size: x-small;"><span style="color: #0000ff; font-size: x-small;">string<&#47;span><&#47;span><span style="font-size: x-small;"> newstatus { <&#47;span><span style="color: #0000ff; font-size: x-small;"><span style="color: #0000ff; font-size: x-small;">get<&#47;span><&#47;span><span style="font-size: x-small;">; <&#47;span><span style="color: #0000ff; font-size: x-small;"><span style="color: #0000ff; font-size: x-small;">set<&#47;span><&#47;span><span style="font-size: x-small;">; }<&#47;span><&#47;em><br />
<em><span style="color: #0000ff; font-size: x-small;"><span style="color: #0000ff; font-size: x-small;"> public<&#47;span><&#47;span><span style="font-size: x-small;"> <&#47;span><span style="color: #0000ff; font-size: x-small;"><span style="color: #0000ff; font-size: x-small;">string<&#47;span><&#47;span><span style="font-size: x-small;"> childID { <&#47;span><span style="color: #0000ff; font-size: x-small;"><span style="color: #0000ff; font-size: x-small;">get<&#47;span><&#47;span><span style="font-size: x-small;">; <&#47;span><span style="color: #0000ff; font-size: x-small;"><span style="color: #0000ff; font-size: x-small;">set<&#47;span><&#47;span><span style="font-size: x-small;">; }<&#47;span><&#47;em><br />
<em><span style="color: #0000ff; font-size: x-small;"><span style="color: #0000ff; font-size: x-small;"> public<&#47;span><&#47;span><span style="font-size: x-small;"> <&#47;span><span style="color: #0000ff; font-size: x-small;"><span style="color: #0000ff; font-size: x-small;">string<&#47;span><&#47;span><span style="font-size: x-small;"> parentPIN { <&#47;span><span style="color: #0000ff; font-size: x-small;"><span style="color: #0000ff; font-size: x-small;">get<&#47;span><&#47;span><span style="font-size: x-small;">; <&#47;span><span style="color: #0000ff; font-size: x-small;"><span style="color: #0000ff; font-size: x-small;">set<&#47;span><&#47;span><span style="font-size: x-small;">; }<&#47;span><&#47;em><br />
<em>}<&#47;em><&#47;pre><br />
Insert some data into my collection, and zip zam wazzle, I gots me some cards!</p>
<p>Of course I don't poof my data out of thin air, I actually pull it from the database and stick it into this collection.&nbsp; But that's another story,<br />
less wazzle's, but still a lot of zip's.</p>
