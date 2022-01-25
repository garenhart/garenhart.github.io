---
layout: collection
title: "Quotes by Author"
permalink: /authors_1/
#header:
#    image: "/assets/images/crown-molding-narrow.png"
---
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
.accordion {
  background-color: #eee;
  color: #444;
  cursor: pointer;
  padding: 8px;
  width: 100%;
  border: none;
  text-align: left;
  outline: none;
  font-size: 24px;
  transition: 0.4s;
}

.active, .accordion:hover {
  background-color: #ccc; 
}

.panel {
  padding: 0 18px;
  display: none;
  background-color: white;
  overflow: hidden;
}
</style>
</head>
<body>

{% assign author_posts = site.posts | group_by: 'author' %}
{% for author_post in author_posts %}
<button class="accordion">{{ author_post.name }}</button>
<div class="panel">
        {% for post in author_post.items %}
        <ul>
          <li>
            <a href='{{ site.baseurl }}{{ post.url }}'>{{ post.title }}</a>
          </li>
        </ul>
        {% endfor %}
</div>
{% endfor %}

<script>
var acc = document.getElementsByClassName("accordion");
var i;

for (i = 0; i < acc.length; i++) {
  acc[i].addEventListener("click", function() {
    this.classList.toggle("active");
    var panel = this.nextElementSibling;
    if (panel.style.display === "block") {
      panel.style.display = "none";
    } else {
      panel.style.display = "block";
    }
  });
}
</script>

</body>
</html>
