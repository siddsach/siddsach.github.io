---
layout: archive
title: "Work for Flipside"
permalink: /publications/
author_profile: true
---

![alt text](/images/flipsidelog.png?raw=true)

Flipside is an AI-based opinion platform that makes it easier to learn about different perspectives. You can [learn more about us](https://siddsach.github.io/publications/flipside-1/) or checkout our [research](https://siddsach.github.io/publications/flipside-2/).

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
    {% include archive-single.html %}
{% endfor %}
