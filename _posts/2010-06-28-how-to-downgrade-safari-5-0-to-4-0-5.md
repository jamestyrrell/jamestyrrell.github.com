---
title: How to downgrade Safari 5.0 to 4.0.5
author: james
layout: post
permalink: /2010/06/28/how-to-downgrade-safari-5-0-to-4-0-5/
views:
  - 2012
categories:
  - GWT
---
# 

I recently started to get back into GWT development and was shocked to find that my app kept freezing in Development Mode whilst using Safari on my MacBook Pro. The problem didn’t seem to occur in Firefox just Safari. So I searched using the symptoms as my guide “gwt dev mode crash safari 5″ and lo and behold someone has already reported the [issue][1].

 [1]: http://code.google.com/p/google-web-toolkit/issues/detail?id=5011 "GWT OOPHM Plugin exceptions with Safari 5, OS X v10.6.3 "

The submitter was using 10.6.3 and I am using 10.6.4 but the procedure should be the same.

1.  Download [Pacifist][2] and [Safari 4.0.5][3] (when I downloaded it from Apple it was really slow)
2.  Open Pacifist, do this first so by the time you need to use it the 15 second delay has ellapsed
3.  Mount the Safari 4.0.5 image and open the Safari 4.0.5 package (Safari4.0.5SnowLeopard.pkg) with Pacifist. You can do this either by dragging the package on top of the Pacifist window or icon.
4.  Once open select the first item in the list and click the “Install” button at the top.
5.  A pop-up will appear, tick the “Use Administrator Privileges” box and press the “Install” button
6.  Another pop-up should appear telling you that the “Application already exists”, just tick “Don’t ask again for this installation” box and press the “Replace” button
7.  It will probably tell you a couple more times that a file already exists in which case just repeat step 6.

 [2]: http://www.charlessoft.com/ "Pacifist"
 [3]: http://support.apple.com/kb/dl877 "Safari 4.0.5"

Once the installation is complete you will be back in Safari 4.0.5 land and able to use Dev Mode on your Mac!