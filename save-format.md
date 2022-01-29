---
pagination: enabled: true
layout: home
---

<div class="post-links">
  {% for post in site.posts %}
    
    <div class="post-links">
      <a href= "{{ post.medium-site }}" style="font-size: 40px; text-decoration: none">
        {{ post.title }}
      </a>
      <br>
      {% for tag in post.tags %}
        <a class="tag" href="got">{{tag}}</a>
      {% endfor %}
      <div class="post-excerpt">
        {{ post.content | strip_html | truncatewords: 25 }}
      </div>
      <br>
      - <time datetime="{{ post.date | date: "%Y-%m-%d" }}">{{ post.date | date_to_long_string }}</time>
      <br>
    </div>
  {% endfor %}
</div>

