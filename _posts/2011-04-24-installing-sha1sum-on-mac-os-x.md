---
title: Installing sha1sum on Mac OS X
author: james
layout: post
permalink: /2011/04/24/installing-sha1sum-on-mac-os-x/
views:
  - 1919
categories:
  - Roo
  - Snow Leopard
---
# 

A tool that we use on the Roo project which provides a \_fairly\_ platform neutral sha1 hashing mechanism is sha1sum. The problem is that this tool isn’t included on Mac OS X. I have found a number of posts on the net on the topic of installing sha1sum on Mac OS, but all seem to reference outdated sources and in addition to this installation ends with an error.

To have the latest and greatest sha1sum on your Mac with no error upon installation all you need to do is the following:

1.  Download the latest GNU Core Utilities from [here][1]
2.  Decompress it and run “./configure –prefix=/usr” this will install sha1sum to the standard directory instead of “/usr/local/bin”. You can of course install the latter, but using “/usr” will cause a number of other tools to be updated in the process of install sha1sum.
3.  Run “sudo make && make install”

 [1]: ftp://mirrors.kernel.org/gnu/coreutils/ "coreutils"

You may find that you need to install gcc and a few other dependencies to compile the code. The easiest way of doing this is downloading Xcode. If you are not up for paying for Xcode you can always just install each missing dependency, though this can be a tad tedious.