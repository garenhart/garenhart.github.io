---
layout: collection
title: "Quotes by Author"
permalink: /authors/
author_profile: true
---

<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
ul, #myUL {
  list-style-type: none;
}

#myUL {
  margin: 0;
  padding: 0;
}

.caret {
  cursor: pointer;
  -webkit-user-select: none; /* Safari 3.1+ */
  -moz-user-select: none; /* Firefox 2+ */
  -ms-user-select: none; /* IE 10+ */
  user-select: none;
}

.caret::before {
  content: "\25B6";
  color: #00adb5;
  display: inline-block;
  margin-right: 6px;
}

.caret-down::before {
  -ms-transform: rotate(90deg); /* IE 9 */
  -webkit-transform: rotate(90deg); /* Safari */'
  transform: rotate(90deg);  
}

.nested {
  display: none;
}

.active {
  display: block;
}
</style>
</head>
<body>
{% assign author_posts = site.posts | group_by: 'author' %}
{% for author_post in author_posts %}
{% if author_post.name != 'Garen' %} <!-- exclude myself from authors list while preserving my profile  -->
  <ul id="myUL">
    <li><span class="caret">{{ author_post.name }}</span>
      <ul class="nested">
      {% for post in author_post.items %}
          <!-- GH This block is replaced by the line below to show beginning of posts like in other pages  <li>
              <a href='{{ site.baseurl }}{{ post.url }}'>{{ post.title }}</a>
            </li> -->
        {% include archive-single.html type=entries_layout %}
      {% endfor %}
      </ul>
    </li>
  </ul>
{% endif %}
{% endfor %}

<script>
var toggler = document.getElementsByClassName("caret");
var i;

for (i = 0; i < toggler.length; i++) {
  toggler[i].addEventListener("click", function() {
    this.parentElement.querySelector(".nested").classList.toggle("active");
    this.classList.toggle("caret-down");
  });
}
</script>

</body>
</html>
