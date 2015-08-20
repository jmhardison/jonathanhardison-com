---
layout: post
status: publish
published: true
title: Xceed WPF DataGrid 3.2 Released! Joy Joy of all Joys!
author:
  display_name: Jonathan
  login: jmhadmin
  email: jmh@jonathanhardison.com
  url: ''
author_login: jmhadmin
author_email: jmh@jonathanhardison.com
wordpress_id: 207
wordpress_url: http://www.jonathanhardison.com/?p=207
date: '2009-06-15 08:36:10 -0500'
date_gmt: '2009-06-15 14:36:10 -0500'
categories:
- Uncategorized
tags: []
comments: []
---
<p><img class="alignnone size-full wp-image-208" title="p_datagrid-wpf_pro_en" src="http:&#47;&#47;www.jonathanhardison.com&#47;wp-content&#47;uploads&#47;2009&#47;06&#47;p_datagrid-wpf_pro_en.jpg" alt="p_datagrid-wpf_pro_en" width="246" height="144" &#47;>Xceed Datagrid 3.2 has been released, and the world will know true bliss... ok, my hearty words are lacking today, tired and not enough coffee as I was up waiting for this release.</p>
<p>Xceed DataGrid has been one of those products that not only "Just Works" but solidly provides a reliable, professional component that your application will a lot of times pivot on. I mean, what else would you display your data to users in? A listview? Come on, that's so 1997.</p>
<p>I haven't installed the update yet, but will shortly and post my drooling response. Below is a recap from their website as to the fixes and new features.</p>
<p>Head on over to their website and pick up yourself a tummy pleasing copy, standard and pro are both out now. <a href="http:&#47;&#47;www.xceed.com" target="_blank">www.xceed.com<&#47;a></p>
<blockquote><p>Version 3.2 features improvements to the datagrid's data virtualization capabilities (grouping, support for data sources implementing IQueryable (LINQ), support for inserting and deleting items with InsertionRow and DeleteCommand), support for Entity Framework data sources, the ability to customize the contents of the AutoFilterControl, auto-detection of ComboBox columns (enums, foreign keys), custom key-value mappings, support for unbound data fields, and direct support for unbound columns. Finally, SP1 of .NET Framework 3.5 is now targeted.<&#47;blockquote></p>
<blockquote><p><span style="line-height: normal;"><span style="font-size: medium;"><span></p>
<table border="0" cellspacing="0" cellpadding="0">
<tbody>
<tr>
<td align="left" valign="top"><span class="Text">New version (3.2)<&#47;span><&#47;td></p>
<td align="left" valign="top">
<ul>
<li>Added&nbsp;<a href="http:&#47;&#47;xceed.com&#47;Grid_WPF_New.html">new features<&#47;a>.<&#47;li>
<li>Added DataGridControl.SelectionChanged event. &nbsp;<strong><-----HOLY CRAP YES!<&#47;strong><&#47;li>
<li>MaskedTextBox now works properly with IME input.<&#47;li>
<li>An exception no longer occurs when a data item has more than one level of details.<&#47;li>
<li>The AutoFilterControl now displays properly in high contrast.<&#47;li>
<li>An exception no longer occurs when inserting new data via the InsertionRow when the data source is List&nbsp;or DataTable.<&#47;li>
<li>HierarchicalGroupByControl.Background property now works in the Aero theme.<&#47;li>
<li>A layout problem no longer occurs in the InsertionRow when changing the DataGrid's theme while the InsertionRow is being edited.<&#47;li>
<li>Focus events are now raised properly by the DataGridControl.<&#47;li>
<li>Resource Center now properly detects the installed samples on 64-bit Windows.<&#47;li>
<li>Added IsAlternatingRowStyleEnabled property to PrintView.<&#47;li>
<li>An exception no longer occurs when changing the DataGrid's theme while a detail row is being edited.<&#47;li>
<li>Calling DataGridCollectionView.Refresh now properly refreshes the StatFunctions.<&#47;li>
<li>An exception no longer occurs when removing a DataRow from an expanded group which is itself in a collapsed group.<&#47;li>
<li>Setting e.Cancel to True in Cell.EditEnding event handler no longer allows an invalid value to be set to the cell.<&#47;li>
<li>The AutoFilterControl no longer interprets underscore characters as Access Keys.<&#47;li>
<li>Cells that are part of an invisible column are now recycled properly.<&#47;li>
<li>Column auto-sizing now works properly when there is more than one detail grid per level.<&#47;li>
<li>When the data source raises an item moved event, the DataGrid now refreshes properly.<&#47;li>
<li>The CurrentItem no longer occasionally changes after the data source raises a Replace event.<&#47;li>
<li>Fixed a cell layout problem that occurs when a cell being edited is scrolled out of view.<&#47;li>
<li>Editing two DataGrids on two different threads no longer throws an exception.<&#47;li>
<li>A binding error no longer occurs when collapsing a detail grid while it is not completely visible.<&#47;li>
<li>The DataGrid now refreshes properly when Groups are added or removed from detail grids.<&#47;li>
<li>When bound to a DataTable, the DataGrid now accesses the DataRowViews instead of their underlying DataRows.<&#47;li>
<li>AutoCreateDetailDescriptions property has been moved from DataGridCollectionViewSource to DataGridCollectionViewSourceBase.<&#47;li>
<li>NumericTextBox now correctly supports the Byte ValueDataType.<&#47;li><br />
<&#47;ul><br />
<&#47;td><br />
<&#47;tr><br />
<&#47;tbody><&#47;table><br />
<&#47;span><&#47;span><&#47;span><&#47;blockquote></p>
