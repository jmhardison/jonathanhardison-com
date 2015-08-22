---
layout: post
status: publish
published: true
title: NeatWorks 4.x on Windows 7 RTM.
author:
  display_name: Jonathan
  login: jmhadmin
  email: jmh@jonathanhardison.com
  url: ''
author_login: jmhadmin
author_email: jmh@jonathanhardison.com
wordpress_id: 224
wordpress_url: http://www.jonathanhardison.com/?p=224
date: '2009-08-10 09:00:56 -0500'
date_gmt: '2009-08-10 15:00:56 -0500'
categories:
- Software
- Windows
tags:
- LinkedIn
comments: []
---
I have finished testing The Neat Companies NeatWorks 4.6.2_152 product  on a fresh install of Windows 7 Ultimate (32bit and 64bit).  Through this process I have found that during install if you fail to run the  initial install as an administrator, you will need to perform an additional  step to get the database running correctly. The install will complete  successfully, or at least appear that way even if you don’t do the install  as an administrator.

Now first of all, by run it as administrator I am an administrator, but  this is specifically if you have UAC still turned on. Since under UAC even  an administrator is not an administrator without saying you want to be.

So to run the initial install as an administrator, you simiply right click  on the file and click ‘Run as Administrator’. That’s it!  Now if you forget that step or don’t even think about it, you will make it  through but then receive errors along the lines of:


8/8/2009 10:11:43 AM MDIParent Main
Machine Info :    OS: Microsoft Windows NT 6.1.7600.0    .NET CLR: 2.0.50727.4927
Assembly Base: file:///C:/Program Files/NeatWorks/exec/NeatWorks.exe
Assembly Name: NeatWorks, Version=4.6.2.146, Culture=neutral, PublicKeyToken=null
Assembly Vers: 4.6.2.146
Error Message: Cannot open database “nrprofessional” requested by the login. The login failed.
Login failed for user ‘sa’.
Exception Type: System.Data.SqlClient.SqlException
Target Site  : GetConnection
–StackTrace–:    at System.Data.ProviderBase.DbConnectionPool.GetConnection  (DbConnection owningObject)
at System.Data.ProviderBase.DbConnectionFactory.GetConnection(DbConnection owningConnection)
at System.Data.ProviderBase.DbConnectionClosed.OpenConnection(DbConnection outerConnection,  DbConnectionFactory connectionFactory)
at System.Data.SqlClient.SqlConnection.Open()
at NeatReceipts.Components.Database.DBConnection.GetConnection()
at com.digitalbp.state.ccSystemSession.firstLoginCheck()
at com.digitalbp.state.ccSystemSession..ctor()
at Program.SetupUserSession()
at Program.Main(String[] args)
User Message : Cannot open database “nrprofessional” requested by the login. The login failed.  Login failed for user ‘sa’.
8/8/2009 10:11:43 AM MDIParent Main
