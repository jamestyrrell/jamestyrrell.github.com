---
title: How to dump/export the contents of Frontbase.
author: james
layout: post
permalink: /2010/06/24/how-to-dump-the-contents-of-frontbase/
views:
  - 819
categories:
  - Random
---
# 

Often when moving between Frontbase versions or platforms you need to dump the contents of the database in order to migrate the data over, the traditional backup doesn’t work.

1.  Launch Frontbase Manager
2.  Connect to the database you want to dump
3.  Select the “SQL Interpreter” list item
4.  Type in “write all output(dir=’/FrontBaseBackup’, type = ‘FrontBase’, content=true);”

To restore, you just need to execute the “schema.sql”.