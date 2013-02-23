---
title: Mac OS X Leopard SpringSource tcServer with AMS
author: james
layout: post
permalink: /2009/06/09/mac-os-x-leopard-springsource-tcserver-with-ams/
views:
  - 588
categories:
  - Random
---
# 

I have just successfully installed this after a couple of hours of headaches.

I was receiving errors along the lines of “cannot execute binary file” etc, and the inbuilt database was failing to start which subsequently caused the installation to fail.

I fixed the problem by:

1.  Defining JAVA_HOME in ~/.profile
2.  Choosing the full setup option and using PostgresSQL instead of the inbuilt db
3.  Removing the included JRE i.e. deleting YOUR\_SERVER\_HOME/server-2.0.0/jre

All fixed now!