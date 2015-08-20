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
<p>I have finished testing The Neat Companies NeatWorks 4.6.2_152 product<br />
on a fresh install of Windows 7 Ultimate (32bit and 64bit).<br />
Through this process I have found that during install if you fail to run the<br />
initial install as an administrator, you will need to perform an additional<br />
step to get&nbsp;the database running correctly. The install will complete<br />
successfully, or at least appear that way even if you don't do the install<br />
as an administrator.</p>
<p>Now first of all, by run it as administrator I am an administrator, but<br />
this is specifically if you have UAC still turned on. Since under UAC even<br />
an administrator&nbsp;is not an administrator without saying you want to be.</p>
<p>So to run the initial install as an administrator, you simiply right click<br />
on the file and click 'Run as Administrator'. That's it!<br />
Now if you forget that step or don't even think about it, you will make it<br />
through but then receive errors along the lines of:</p>
<div>
<blockquote>
<div>8&#47;8&#47;2009 10:11:43 AM MDIParent Main<&#47;div></p>
<div>Machine Info : &nbsp; &nbsp;OS: Microsoft Windows NT 6.1.7600.0 &nbsp; &nbsp;.NET CLR: 2.0.50727.4927<&#47;div></p>
<div>Assembly Base: file:&#47;&#47;&#47;C:&#47;Program Files&#47;NeatWorks&#47;exec&#47;NeatWorks.exe<&#47;div></p>
<div>Assembly Name: NeatWorks, Version=4.6.2.146, Culture=neutral, PublicKeyToken=null<&#47;div></p>
<div>Assembly Vers: 4.6.2.146<&#47;div></p>
<div>Error Message: Cannot open database "nrprofessional" requested by the login. The login failed.<&#47;div></p>
<div>Login failed for user 'sa'.<&#47;div></p>
<div>Exception Type: System.Data.SqlClient.SqlException<&#47;div></p>
<div>Target Site &nbsp;: GetConnection<&#47;div></p>
<div>--StackTrace--: &nbsp; &nbsp;at System.Data.ProviderBase.DbConnectionPool.GetConnection<br />
(DbConnection owningObject)<&#47;div></p>
<div>at System.Data.ProviderBase.DbConnectionFactory.GetConnection(DbConnection owningConnection)<&#47;div></p>
<div>at System.Data.ProviderBase.DbConnectionClosed.OpenConnection(DbConnection outerConnection,<br />
DbConnectionFactory connectionFactory)<&#47;div></p>
<div>at System.Data.SqlClient.SqlConnection.Open()<&#47;div></p>
<div>at NeatReceipts.Components.Database.DBConnection.GetConnection()<&#47;div></p>
<div>at com.digitalbp.state.ccSystemSession.firstLoginCheck()<&#47;div></p>
<div>at com.digitalbp.state.ccSystemSession..ctor()<&#47;div></p>
<div>at Program.SetupUserSession()<&#47;div></p>
<div>at Program.Main(String[] args)<&#47;div></p>
<div>User Message : Cannot open database "nrprofessional" requested by the login. The login failed.<br />
Login failed for user 'sa'.<&#47;div><&#47;blockquote><br />
<&#47;div></p>
<div><span style="color: #000000;"></p>
<div id="_mcePaste" style="position: absolute; left: -10000px; top: 0px; width: 1px; height: 1px; overflow-x: hidden; overflow-y: hidden;">8&#47;8&#47;2009 10:11:43 AM MDIParent Main<&#47;div></p>
<div id="_mcePaste" style="position: absolute; left: -10000px; top: 0px; width: 1px; height: 1px; overflow-x: hidden; overflow-y: hidden;">Machine Info : &nbsp; &nbsp;OS: Microsoft Windows NT 6.1.7600.0 &nbsp; &nbsp;.NET CLR: 2.0.50727.4927<&#47;div></p>
<div id="_mcePaste" style="position: absolute; left: -10000px; top: 0px; width: 1px; height: 1px; overflow-x: hidden; overflow-y: hidden;">Assembly Base: file:&#47;&#47;&#47;C:&#47;Program Files&#47;NeatWorks&#47;exec&#47;NeatWorks.exe<&#47;div></p>
<div id="_mcePaste" style="position: absolute; left: -10000px; top: 0px; width: 1px; height: 1px; overflow-x: hidden; overflow-y: hidden;">Assembly Name: NeatWorks, Version=4.6.2.146, Culture=neutral, PublicKeyToken=null<&#47;div></p>
<div id="_mcePaste" style="position: absolute; left: -10000px; top: 0px; width: 1px; height: 1px; overflow-x: hidden; overflow-y: hidden;">Assembly Vers: 4.6.2.146<&#47;div></p>
<div id="_mcePaste" style="position: absolute; left: -10000px; top: 0px; width: 1px; height: 1px; overflow-x: hidden; overflow-y: hidden;">Error Message: Cannot open database "nrprofessional" requested by the login. The login failed.<&#47;div></p>
<div id="_mcePaste" style="position: absolute; left: -10000px; top: 0px; width: 1px; height: 1px; overflow-x: hidden; overflow-y: hidden;">Login failed for user 'sa'.<&#47;div></p>
<div id="_mcePaste" style="position: absolute; left: -10000px; top: 0px; width: 1px; height: 1px; overflow-x: hidden; overflow-y: hidden;">Exception Type: System.Data.SqlClient.SqlException<&#47;div></p>
<div id="_mcePaste" style="position: absolute; left: -10000px; top: 0px; width: 1px; height: 1px; overflow-x: hidden; overflow-y: hidden;">Target Site &nbsp;: GetConnection<&#47;div></p>
<div id="_mcePaste" style="position: absolute; left: -10000px; top: 0px; width: 1px; height: 1px; overflow-x: hidden; overflow-y: hidden;">--StackTrace--: &nbsp; &nbsp;at System.Data.ProviderBase.DbConnectionPool.GetConnection(DbConnection owningObject)<&#47;div></p>
<div id="_mcePaste" style="position: absolute; left: -10000px; top: 0px; width: 1px; height: 1px; overflow-x: hidden; overflow-y: hidden;">at System.Data.ProviderBase.DbConnectionFactory.GetConnection(DbConnection owningConnection)<&#47;div></p>
<div id="_mcePaste" style="position: absolute; left: -10000px; top: 0px; width: 1px; height: 1px; overflow-x: hidden; overflow-y: hidden;">at System.Data.ProviderBase.DbConnectionClosed.OpenConnection(DbConnection outerConnection, DbConnectionFactory connectionFactory)<&#47;div></p>
<div id="_mcePaste" style="position: absolute; left: -10000px; top: 0px; width: 1px; height: 1px; overflow-x: hidden; overflow-y: hidden;">at System.Data.SqlClient.SqlConnection.Open()<&#47;div></p>
<div id="_mcePaste" style="position: absolute; left: -10000px; top: 0px; width: 1px; height: 1px; overflow-x: hidden; overflow-y: hidden;">at NeatReceipts.Components.Database.DBConnection.GetConnection()<&#47;div></p>
<div id="_mcePaste" style="position: absolute; left: -10000px; top: 0px; width: 1px; height: 1px; overflow-x: hidden; overflow-y: hidden;">at com.digitalbp.state.ccSystemSession.firstLoginCheck()<&#47;div></p>
<div id="_mcePaste" style="position: absolute; left: -10000px; top: 0px; width: 1px; height: 1px; overflow-x: hidden; overflow-y: hidden;">at com.digitalbp.state.ccSystemSession..ctor()<&#47;div></p>
<div id="_mcePaste" style="position: absolute; left: -10000px; top: 0px; width: 1px; height: 1px; overflow-x: hidden; overflow-y: hidden;">at Program.SetupUserSession()<&#47;div></p>
<div id="_mcePaste" style="position: absolute; left: -10000px; top: 0px; width: 1px; height: 1px; overflow-x: hidden; overflow-y: hidden;">at Program.Main(String[] args)<&#47;div></p>
<div id="_mcePaste" style="position: absolute; left: -10000px; top: 0px; width: 1px; height: 1px; overflow-x: hidden; overflow-y: hidden;">User Message : Cannot open database "nrprofessional" requested by the login. The login failed.Login failed for user 'sa'.<&#47;div><br />
<&#47;span><&#47;div><br />
<span style="color: #339966;"> <&#47;span><span style="color: #339966;"><span style="color: #000000;">In this case you will need to do one item over again, or you could uninstall and reinstall, but that will take<br />
a lot longer.<&#47;span><&#47;span> So lets begin!</p>
<ol>
<li>Open the path: %Program Files%Common FilesThe Neat CompanySetup<&#47;li>
<li>Right click on 'Neat Database Setup.exe' and select 'Run as Administrator'<br />
<img class="alignnone size-full wp-image-225" title="CaptureNRfix" src="http:&#47;&#47;www.jonathanhardison.com&#47;wp-content&#47;uploads&#47;2009&#47;08&#47;CaptureNRfix.PNG" alt="CaptureNRfix" width="415" height="400" &#47;><&#47;li></p>
<li>Complete the following install as normal, and upon completion your database will now<br />
be working and you can launch NeatWorks without an issue.<&#47;li><br />
<&#47;ol><br />
If you have for some reason not done a fresh install of Windows 7, but instead have<br />
performed an upgrade... the one issue I have noticed is a delay in starting the<br />
'Database Controller Service' before the SQL instance is started. Other than running<br />
services.msc, you can also check in one location for NeatWorks status. You may open the<br />
'Support Center' by  Expanding Networks and Support Tools, then clicking on "Neat Support Center" in your start menu.<br />
<img class="alignnone size-full wp-image-226" title="CaptureNRMenu" src="http:&#47;&#47;www.jonathanhardison.com&#47;wp-content&#47;uploads&#47;2009&#47;08&#47;CaptureNRMenu.PNG" alt="CaptureNRMenu" width="229" height="131" &#47;></p>
<p>This program will let you view log files from the application, as well as submit support<br />
information to The Neat Company. But one tab in particular is a simple view of your NeatWorks<br />
related services. A note about this screen, on Windows 7 it will still say the OS is Vista.<br />
But the version number will be correct, it is simply the application does not know what Windows 7 is.<br />
<a href="http:&#47;&#47;www.jonathanhardison.com&#47;wp-content&#47;uploads&#47;2009&#47;08&#47;CaptureSupportTools.PNG" target="_blank"><img class="alignnone size-full wp-image-227" style="border: 0px initial initial;" title="CaptureSupportTools" src="http:&#47;&#47;www.jonathanhardison.com&#47;wp-content&#47;uploads&#47;2009&#47;08&#47;CaptureSupportTools.PNG" alt="CaptureSupportTools" width="687" height="655" &#47;><&#47;a></p>
