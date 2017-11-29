---
layout: post
title:  "Trust Root CA in Windows Container"
date:   2017-11-29 01:00:00
categories: general
author: Jonathan
comments: true
share:
---

If you are at an enterprise, you are more than likely going to experience the joys of having SSL inspection in-line of your system to the Internet. For good or bad, I won't argue its merrits right now but lets look at one of the fun issues that crops up.

Enter containers on windows.

Lets say you are building a container, for example a windows based container that performs a dotnet restore and build. Part of that restore process will be to download missing packages using NuGet. Unfortunately NuGet doesn't have a configuration file entry to ignore certificate validation errors, and you may not be in an environment where you can specify the proxy address for SSL connection.

No problem, we can fix the SSL errors by doing what we would normally do... trusting the root cert.

So to do this, you will need to get your hands on the cert and its chain. If you are on a machine that trusts it, you should be able to find it in your computers tr


  * Open MMC, add the certificates snap-in and manage "Computer Account".
  * Locate the certificate that is used by your SSL Inspection appliance under "Trusted Root Certification Authorities".
  * Right click on the item, and under all tasks select "export".
  * In your options for the export, select "Cryptographic Message Syntax Standard - PKCS #7 Certificates (.P7B)" and tick "Include all certificates in the certification path if possible".
  * Export to a p7b file in your project folder with the Dockerfile. (ex: sslinpsect.p7b)
  * Add the following lines to your Dockerfile before any action that will consume Internet resources.  
     ```Dockerfile
     ADD sslinspect.p7b .
     RUN import-certificate -filepath sslinspect.p7b -certstorelocation Cert:\LocalMachine\Root
     ```

Now when you build your container any action that was failing due to trust (for example dotnet restore resulting in an error C:\Program Files\dotnet\sdk\2.0.3\NuGet.targets(102,5): error :   A security error occurred ) should work.

