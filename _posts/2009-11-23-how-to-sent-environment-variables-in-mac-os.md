---
title: How to set environment variables in Mac OS
author: james
layout: post
permalink: /2009/11/23/how-to-sent-environment-variables-in-mac-os/
views:
  - 729
categories:
  - Snow Leopard
---
# 

Every time I need to set an environment variable in Mac, e.g. JAVA\_HOME, GWT\_HOME, I always end up turning to Google to find out which file I need to edit; because there are just so my plists! (the file you are meant to edit is here, ~/.MacOSX/environment.plist, and yes create the folder and file if it doesn’t exist and  you will need to logout and then in to apply the change)

This time I stumbled across [RCEnvironment][1], by Doug McClure. This has to be the most useful preference pane in existence. It adds a preference pane to System Settings that lets you easily add environment variables.

 [1]: http://www.rubicode.com/Software/RCEnvironment/ "RCEnvironment"

![RCEnvironment Pref Pane][2]

 [2]: /assets/images/2009/11/RCEnvironment-Pref-Pane.png "RCEnvironment Pref Pane"