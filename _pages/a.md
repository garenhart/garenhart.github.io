---
layout: collection
title: "A (page placeholder for future use :)"
permalink: /A/
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
  color: #00adb5;
  font-size: 30px;

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
  color: none;
  font-size: none;
}

.active {
  display: block;
}
</style>
</head>
<body>
  <ul id="myUL">
    <li><span class="caret">is unique because she</span>
      <ul class="nested">
          <li>item 1</li>
          <li>item 2</li>
      </ul>
    </li>
  </ul>

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
