---
pagination: enabled: true
layout: home
---


<ul>
  {% for post in site.posts %}
    <a>
      <a href= "https://pepper-boi.github.io{{ post.url }}">
        {{ post.title }}
      </a>
      <br></br>
      - <time datetime="{{ post.date | date: "%Y-%m-%d" }}">{{ post.date | date_to_long_string }}</time>
      <br></br>
    </a>
  {% endfor %}
</ul>
