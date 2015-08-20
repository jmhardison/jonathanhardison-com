---
layout: post
status: publish
published: true
title: Acronis True Image 2011 Restore Of MBR Partition to GPT Drive.
author:
  display_name: Jonathan
  login: jmhadmin
  email: jmh@jonathanhardison.com
  url: ''
author_login: jmhadmin
author_email: jmh@jonathanhardison.com
wordpress_id: 554
wordpress_url: http://www.jonathanhardison.com/?p=554
date: '2010-10-09 22:25:39 -0500'
date_gmt: '2010-10-10 04:25:39 -0500'
categories:
- Uncategorized
tags: []
comments: []
---
<p>While toying around with the infamous "install mac retail on a pc" project. I had come across an item that is worth note. This item is when you are wanting to restore your old image created with Acronis True Image 2011. (With plus pack.)</p>
<p>Basically, if you want to restore an image of a partition that was created from an MBR disk to a disk formatted as GPT (Guid Partition Table) then you are unable to resize the partition up or down durring restore. This item came to my face a little to late, but none the less I consider it important enought o post on here. Maybe to save someone else who didn't dig deep into the docs of Acronis.</p>
<p>If you need to restore a partition created on MBR to a GPT disk, be sure the partition you want to restore to already exists. As well as the size of that partition is sufficient to handle the restored image.</p>
