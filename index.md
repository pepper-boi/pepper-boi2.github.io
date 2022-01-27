---
pagination: enabled: true
layout: home
---


<ul>
  {% for post in site.posts %}
    <a>
      <h1 href= "https://pepper-boi.github.io{{ post.url }}">
        {{ post.title }}
      </h1>
      <br>
      - <time datetime="{{ post.date | date: "%Y-%m-%d" }}">{{ post.date | date_to_long_string }}</time>
      <br>
    </a>
  {% endfor %}
</ul>
