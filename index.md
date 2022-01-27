---
pagination: enabled: true
layout: home
---

{% for post in site.posts %}
  <a>
    <a href= "https://pepper-boi.github.io{{ post.url }}" style="font-size: 100px; text-decoration: none">
      {{ post.title }}
    </a>
    <br>
    - <time datetime="{{ post.date | date: "%Y-%m-%d" }}">{{ post.date | date_to_long_string }}</time>
    <br>
  </a>
{% endfor %}

<span>[
  {% for tag in page.tags %}
    {% capture tag_name %}{{ tag }}{% endcapture %}
    <a href="/tag/{{ tag_name }}"><code class="highligher-rouge"><nobr>{{ tag_name }}</nobr></code>&nbsp;</a>
  {% endfor %}
]</span>
