---
title: 'Downgrade Safari from 4.0.4 -> 4.0.3 to get GWT working!'
author: james
layout: post
permalink: /2009/11/13/downgrade-safari-from-404-to-get-gwt-working/
views:
  - 1826
categories:
  - Random
---
# 

As noted here [Issue 4220 – google-web-toolkit – GWT crash (Safari 4.0.4 …][1] and [Issue 4091 – google-web-toolkit – Invalid memory access of …][2], Safar 4.0.4 breaks GWT’s hosted mode.

 [1]: http://code.google.com/p/google-web-toolkit/issues/detail?id=4220
 [2]: http://code.google.com/p/google-web-toolkit/issues/detail?id=4091

You can modify a check within GWT as found here (link broken) or you can just downgrade Safari to 4.0.3.

The files attached come from my MacBook Pro running 10.6.2. I retrieved the files by looking at what was installed in the Safari 4.0.4 update by using Pacifist and then copied the older versions from a backup.

These files are just for Snow Leopard, if you are using Leopard you should just be able to downgrade using the installer ([Safari 4.0.3 Leopard Installer][3]) or the extracted files [Safari Downgrade (Leopard)][4]

 [3]: http://appldnld.apple.com.edgesuite.net/content.info.apple.com/Safari4/061-6723.20090811.DerfT/Safari4.0.3Leo.dmg "Safari 4.0.3 Leopard Installer"
 [4]: /assets/files/2009/11/Safari_downgrade_403_leopard.zip

The files attached are organised as if the folder was your root volume.

[Safari Downgrade][5] (Snow Leopard)

 [5]: /assets/files/2009/11/safari-downgrade.zip

**UPDATE: **Much better solution [here](http://grack.com/blog/2009/11/16/fix-for-gwt-hosted-mode-crash-with-safari-4-0-4/). You won’t have to downgrade. You just have to set an environment variable (see the above post)