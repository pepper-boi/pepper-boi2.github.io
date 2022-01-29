---
pagination: enabled: true
layout: home
---
<h1>recent articles</h1>
<div class="post-links">
      {% for post in site.posts %}
<div class="post-link-wrapper">
<a href="{{ post.url | relative_url }}" class="post-link">{{ post.title }}</a>
<div class="post-meta">
<div class="post-tags">
                {% for tag in post.tags %}
<a class="tag" href="{{ tag | tag_url }}">{{ tag }}</a>
                {% endfor %}
</div>
              {{ post.date | date: site.dash.date_format }}
<div class="post-excerpt">
</div>
</div>
</div>
      {% endfor %}
</div>
    {% include pagination.html %}
    {% include tagcloud.html %}
