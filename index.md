---
layout: page
title: Rajesh S R's blog
---
{% include JB/setup %}

My name is Rajesh S R. I am a Senior Software Engineer in Google.

The purpose of having this blog is sharing my ideas. Sharing not to advertise(ok, that's the secondary motivation! :P), but to be questioned, dissuaded, to get more insights into alternative views etc.
Writing provides a great sense of clarity to your thinking process. So, expect to be spammed with a spaghetti of random thoughts.  As I keep musing, I will post on a variety of topics -- philosophy, cs, society etc. So feel free to comment on that and fight with me, if you think am thinking wrong! :)

As far this blog, i used to maintain a wordpress blog in a .co.cc domain in college, which got lost. I then started using G+ as my blogging platform. But, well, a blog is a blog! You need a way to tag, browse archives etc. So, decided to start my blog again. I am trying out Jekyll as my blogging platform because the model of statically generated blog without any heavy-weighted server side support, looks interesting to me. To start with, I seeded my blog contents from some of my G+ posts and backup of my old blog.


I also have a Quora profile: <http://www.quora.com/Rajesh-S-Rajagopalan>.

Here are my posts:  

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

