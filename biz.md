---
layout: page
title: Business
permalink: /biz
---

<div>
{% for item in site.biz %}
    <a href="{{ item.url }}">
        <h2>{{ item.title }}</h2>
    </a>
{% endfor %}
</div>
