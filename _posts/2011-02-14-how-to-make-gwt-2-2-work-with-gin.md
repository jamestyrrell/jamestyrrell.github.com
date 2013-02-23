---
title: How to make GWT 2.2 work with GIn
author: james
layout: post
permalink: /2011/02/14/how-to-make-gwt-2-2-work-with-gin/
views:
  - 2368
categories:
  - Coding
  - Google
  - GWT
  - Java
  - Roo
  - Spring
---
# 

Whilst not officially announced GWT 2.2 is out and it breaks GIn. To get around this you will need to recompile GIn with GWT 2.2, or, if you are lazy, you can just [download][1] the jar that I prepared earlier ![:)][2] If you choose to recompile GIn yourself you just need to:

 [1]: /files/2011/02/gin-1.0-SNAPSHOT.jar_.zip
 [2]: /assets/images/icon_smile.gif

1.  Checkout GIn, instructions [here][3]
2.  Change you GWT_HOME to point to GWT 2.2, this is just an environment variable
3.  Build GIn via ant by running “ant dist”

 [3]: http://code.google.com/p/google-gin/source/checkout "Checkout GIn"

**Maven tips** (if you aren’t using Maven you are done)

If you are using Maven you will need to manually install the jar using the following command (make sure you replace LOCATION\_OF\_RECOMPILED\_GIN\_JAR with the physical location of the jar you recompiled or downloaded):

 {% highlight bash %}   
    mvn install:install-file -DgroupId=com.googlecode.gwt.inject -DartifactId=gin -Dpackaging=jar \
    -Dversion=1.0-SNAPSHOT -Dfile=LOCATION_OF_RECOMPILED_GIN_JAR/gin-1.0-SNAPSHOT.jar
    {% endhighlight %}

Once you have installed the jar you will need to edit the pom to add in the required dependencies (guice-3.0-rc2 and guice-assistedinject-3.0-rc2), locate your Maven repo and then open “gin-1.0-SNAPSHOT.pom” which is located in your .m2 directory (the default location of your .m2 directory is your user home directory so the file should be located at ~/.m2/repository/com/googlecode/gwt/inject/gin/1.0-SNAPSHOT/gin-1.0-SNAPSHOT.pom) and then add the following just above the closing project tag ():
 
{% highlight xml %}
  <dependencies>
    <dependency>
      <groupId>com.google.inject</groupId>
      <artifactId>guice</artifactId>
      <version>3.0-rc2</version>
    </dependency>
    <dependency>
      <groupId>com.google.inject.extensions</groupId>
      <artifactId>guice-assistedinject</artifactId>
      <version>3.0-rc2</version>
    </dependency>
  </dependencies>
{% endhighlight %}
    	
    

Add that is it. Now you can run your GIn dependent GWT application using GWT 2.2!