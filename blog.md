---
layout: page
title: Blog
permalink: /blog/
---

These are blogposts semi-regularly about professional development and introduction to Machine Learning methodologies for AI enthusiast or practioners interested in Transfer Learning, Natural Language Processing etc. A full listing of the blog posts follows.

<ul id="archive">
{% for post in site.posts %}
  {% capture y %}{{post.date | date:"%Y"}}{% endcapture %}
  {% if year != y %}
    {% assign year = y %}
    <h2 class="blogyear">{{ y}}</h2>
  {% endif %}
<li class="archiveposturl"><span><a href="{{ site.url }}{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a></span><br/>
<span class = "postlower"><strong>Author:</strong> {{post.author}} 
<strong>Category:</strong>  {% if post.categories %}
 
  {% for cat in post.categories %}
  <a href="/categories/#{{ cat }}" title="{{ cat }}">{{ cat }}</a>&nbsp;
  {% endfor %}

{% endif %} <!-- {{ post.categories | first }} -->
<strong style="font-size:100%; font-family: 'Titillium Web', sans-serif; float:right">{{ post.date | date: '%d %b %Y' }}</strong> 
</span> 

</li>
{% endfor %}
</ul>

<!-- {{ post.date | date: '%m %d, %Y' }} -->
