---
title: Install and setup S3cmd on a Mac
author: james
layout: post
permalink: /2011/02/21/install-and-setup-s3cmd-on-a-mac/
views:
  - 4888
categories:
  - Coding
  - Roo
  - Spring
---
# 

The Roo project has recently setup continuous integration (we are currently using Hudson but will soon migrate to Jenkins) to hunt down committers that break the world, push documentation out faster, and reduce the need for developers to wait for final releases or build Roo from master to access fixes. As part of this we leverage S3cmd to automate deploying snapshots to S3. I initially thought that in order to install S3cmd on my Mac I would need to Fink or DarwinPorts it up. Not so. To install and setup S3cmd on a Mac all you to do is:

1.  Download [S3cmd][1] and extract it
2.  Run “sudo python setup.py install” from command.
3.  Finally, run “s3cmd –configure” from command to configure S3cmd.

 [1]: http://s3tools.org/download "Download S3cmd"

And that is it, how simple! Make sure you are not running as root when performing the final step as to not create a config file that is only accessible by a root user.