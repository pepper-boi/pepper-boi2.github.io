---
pagination: enabled: true
layout: home
---

<div class="post-links">
  {% for post in site.posts %}
    <a>
      <a href= "https://pepper-boi.github.io{{ post.url }}" style="font-size: 40px; text-decoration: none">
        {{ post.title }}
      </a>
    </a>
      {% for tag in post.tags}
        <a class="tag" href="got">{{tag}}</a>
      {% endfor %}
    <a>
      - <time datetime="{{ post.date | date: "%Y-%m-%d" }}">{{ post.date | date_to_long_string }}</time>
      <br>
    </a>
  {% endfor %}
</div>
