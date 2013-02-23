---
title: Transparent Tabs GXT (Ext-GWT)
author: james
layout: post
permalink: /2009/06/10/transparent-tabs-gxt-ext-gwt/
views:
  - 947
categories:
  - Random
---
# 

Your project is call myProject then you should have a css file called myProject.css and this css file should be added to your projects html file, etc..

Put this in that css file:
{% highlight css %}
    .transparent .x-tab-panel-body-top {
        background-color: transparent !important;
    }
{% endhighlight %}

then add a the style name to a TabPanel.
{% highlight java %}
    TabPanel tabs = new TabPanel();
    tabs.addStyleName("transparent");
{% endhighlight %}

Inspiration: [ https://extjs.net/forum/showthread.php?p=333588][1]

 [1]: https://extjs.net/forum/showthread.php?p=333588
