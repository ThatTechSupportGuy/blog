---
layout: page
title: Technology
permalink: /technology/
---
{% for post in site.posts%}
{% if post.categories contains 'technology' %}
[{{post.title}}]({{site.baseurl}}{{post.url}})
{% endif %}
{% endfor %}