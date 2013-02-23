---
layout: post
title: Ebean, Postgres and GenerationType.IDENTITY
---

I have been using Ebean with Postgres over the past couple of months without a problem, in fact Ebean has managed to stay completely out of may and I recommend you give it a go in your next project. This was up until last week when I hit my first issue whilst trying to use a stored procedure to generate the primary key for an entity (previously I was just being lazy and using a UUID). This shouldn't be an issue as in JPA GenerationType.IDENTITY exists which allows for an ID to be created by the database on insert, but for whatever reason Ebean disables this option by default so even if you use GenerationType.IDENTITY it will be ignored. Bummer.

To get around this problem you need to provide an altered PostgresPlatform instance when setting up you ServerConfig instance. A highly focused code snipet follows which basically shows what you need to do.

{% highlight java native %}
    final ServerConfig config = new ServerConfig();
        
    final PostgresPlatform postgresPlatform = new PostgresPlatform();
    postgresPlatform.getDbIdentity().setIdType(IdType.IDENTITY);
    postgresPlatform.getDbIdentity().setSupportsIdentity(true);

    config.setDatabasePlatform(postgresPlatform);
{% endhighlight %}

With this bit of code you can now go forward and use a stored procedure to generate your keys just as the instagram peeps do, hurrah!