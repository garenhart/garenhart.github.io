---
layout: collection
title: "Quotes by Author"
permalink: /authors/
header:
    image: "/assets/images/crown-molding-narrow.png"
---

{% assign author_posts = site.posts | group_by: 'author' %}

<ul>
  {% for author_post in author_posts %}

    <li>
      <h2>{{ author_post.name }}</h2>
      <ul>
        {% for post in author_post.items %}
        <li>
          <a href='{{ site.baseurl }}{{ post.url }}'>{{ post.title }}</a>
        </li>
        {% endfor %}
      </ul>
    </li>
  {% endfor %}
</ul>
