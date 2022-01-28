---
pagination: enabled: true
layout: home
---

{% for post in site.posts %}
  <a>
    <a href= "https://pepper-boi.github.io{{ post.url }}" style="font-size: 40px; text-decoration: none">
      {{ post.title }}
    </a>
    <br>
    <a class="tag" href="got">got</a>
<!--     {% for tag in post.tags %}
      <a href="/{{ site.tag_page_dir }}/{{ tag | slugify: 'pretty' }}/">{{ tag }}</a>
    {% endfor %} -->
    - <time datetime="{{ post.date | date: "%Y-%m-%d" }}">{{ post.date | date_to_long_string }}</time>
    <br>
  </a>
{% endfor %}
