---
title: Test Quotes
layout: collection
permalink: /quotes/
collection: quotes
entries_layout: grid
classes: wide
author_profile: false
header:
    image: "/assets/images/crown-molding-narrow.png"
---

[//]: # (need to investigate at some point whether the code below can potentially sort quotes by category)
{% assign groups = site.quotes | group_by: "category" | sort: "name" %}

{% for group in groups %}
    {{ group.name }}
    {% for item in group.items %}
        {{item.abbrev}}
    {%endfor%}
{%endfor%}
