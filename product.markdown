---
layout: page
title: Product
permalink: /product/
---
{% for post in site.posts%}
{% if post.categories contains 'product' %}
[{{post.title}}]({{site.baseurl}}{{post.url}})
{% endif %}
{% endfor %}