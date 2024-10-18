---
layout: page
title: Poetry
#permalink: /poetry/
---
{% for post in site.posts%}
[{{post.title}}]({{post.url}}) {{post.categories}}
{%if post.categories contain 'poetry'%}
{{post.url}}
{%endif%}
{% endfor %}