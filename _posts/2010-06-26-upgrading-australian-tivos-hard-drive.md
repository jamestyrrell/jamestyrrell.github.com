---
title: 'Upgrading an Australian Tivo&#8217;s hard drive'
author: james
layout: post
permalink: /2010/06/26/upgrading-australian-tivos-hard-drive/
views:
  - 1383
categories:
  - Random
---
# 

I have just installed a WD1002FAEX in my Tivo after my GreenPower 1TB hard drive failed. It is working well, nice and fast, though a little noisy.

This is just a brief list of what you need to do. If you have more questions just ask in the comments.

1.  Open Tivo by unscrewing the 6 Torx-15 screws at the back of the unit (you will need a Torx-15 screwdriver)
2.  Remove the hard drive by unscrewing the 4 Torx-15 screws
3.  Remove the hard drive from its caddy (the metal thing) by unscrewing he 4 Torx-15 screws at the base of the drive
4.  Go to a Windows computer and download WinMFS
5.  Plug the drive into a computer via SATA
6.  Open WinMFS and backup the hard drive (in WinMFS go to File->Backup->Tivo Hard Drive)
7.  Shutdown the Windows computer and connect your new drive and power it back up again
8.  Open WinMFS and restore the image to your new drive (in WinMFS go to File->Restore->Tivo Hard Drive – find the image of the backup you made earlier and press restore)
9.  Put everything back together and you are done.