---
layout: post
status: publish
published: true
title: CardView Xceed DataGrid WPF Style!
author: Jonathan
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
So I took a quick break from all the installer creations I’ve been doing lately to enjoy some work on an old project… DCTracker!

I know, it is the neverending project, but when you get little time to work on anything else… blah blah. Ok, so here’s the deal, I wanted to take my Child Attendance program from this:

![old1]({{site.bas}}/imagecontent/2009/05/captureold.jpg)

To this:

![new1]({{site.base}}/imagecontent/2009/05/capturenew.jpg)

Well wouldn’t you know it, that is just super simple in [Xceed DataGrid](http://www.xceed.com){:target="_blank"}.

In the XAML of my window, I clicked “Show Configuration Window” on my datagrid.
Then selected cardview:

![new2]({{site.base}}/imagecontent/2009/05/capturecardviewconfig1.jpg)

After selecting cardview and the theme I desired, I switched to the columns tab and setup my fields.

![new3]({{site.base}}/imagecontent/2009/05/capturecolumns.jpg)

The “Field Name” corresponds to the field name in my dataset I will be passing, whereas “Title” is shown on the card.<br /> Next, we configure the data source in our code:

{% highlight C# %}
dataGridControlChildDisplay.ItemsSource = childListView;
{% endhighlight %}
