---
layout: page
title: Rajesh S R's blog
---
{% include JB/setup %}

My name is Rajesh S R. I am a Senior Software Engineer in Google.

The purpose of having this blog is sharing my ideas. Sharing not to advertise(ok, that's the secondary motivation! :P), but to be questioned, dissuaded, to get more insights into alternative views etc.
Writing provides a great sense of clarity to your thinking process. So, expect to be spammed with a spaghetti of random thoughts.  As I keep musing, I will post on a variety of topics -- philosophy, cs, society etc. So feel free to comment on that and fight with me, if you think am thinking wrong! :)

Here are my posts:  

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>


