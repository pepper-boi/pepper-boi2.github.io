---
pagination: enabled: true
layout: home
---

<!-- {% for post in site.posts %}
  <a>
    <a href= "https://pepper-boi.github.io{{ post.url }}" style="font-size: 100px; text-decoration: none">
      {{ post.title }}
    </a>
    <br>
    - <time datetime="{{ post.date | date: "%Y-%m-%d" }}">{{ post.date | date_to_long_string }}</time>
    <br>
  </a>
{% endfor %} -->

{% for tag in site.tags %}
  <h3>{{ tag[0] }}</h3>
  <ul>
    {% for post in tag[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}
