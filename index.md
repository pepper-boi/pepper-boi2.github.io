---
pagination: enabled: true
layout: home
---


<ul>
  {% for post in site.posts %}
    <li>
      <h2 href="{{ post.url }}">
        {{ post.title }}
      </h2>
      - <time datetime="{{ post.date | date: "%Y-%m-%d" }}">{{ post.date | date_to_long_string }}</time>
    </li>
  {% endfor %}
</ul>
