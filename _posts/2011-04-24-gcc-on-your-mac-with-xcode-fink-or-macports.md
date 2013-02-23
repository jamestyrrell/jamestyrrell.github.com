---
title: GCC on your Mac without Xcode, Fink, or MacPorts
author: james
layout: post
permalink: /2011/04/24/gcc-on-your-mac-with-xcode-fink-or-macports/
views:
  - 2537
categories:
  - Coding
  - Snow Leopard
tags:
  - Development
  - Fink
  - GCC
  - MacPorts
  - Xcode
---
# 

One of the most annoying things about Apple charging for Xcode is that you now need to pay $4.99 for an easy way to setup your dev tool chain on your Mac. You don’t have to pay, there is always Fink or MacPorts but that too involves hassel.

Fortunately, there is now a third **free** option!

All you need to do is install the three packages contained in [this zip][1]. The packages came directly from the Xcode installation package, but as they don’t generally contain Apple specific code I think it is fair to redistribute them as you are not getting the awesome Xcode IDE and associated Developer Tools, you are just getting the bare bones binaries which allow you to such magical things as run “./configure && make && make install”!

 [1]: http://s3.populationjim.com/downloads/AppleDevToolsLight.zip "Apple Dev Tools Light"

N.B. This has only been test on Mac OS 10.6, when 10.7 comes out it is likely that I will need to re-upload the files.