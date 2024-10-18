---
layout: page
title: Poetry
permalink: /poetry/
---
{% for post in site.posts%}
{% if {{post.categories}} contains 'poetry' %}
[{{post.title}}]({{site.baseurl}}{{post.url}})
{% endif %}
{% endfor %}