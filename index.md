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

<!-- ---
layout: default
---
{% unless site.dash.show_author == false %}
  {% include author.html %}
{% endunless %}
{{ content }}
{% assign posts_count = paginator.posts | size %}
{% if posts_count > 0 %}
<h1>recent articles</h1>
    <div class="post-links">
      {% for post in paginator.posts %}
        <div class="post-link-wrapper">
          <a href="{{ post.url | relative_url }}" class="post-link">{{ post.title }}</a>
          <div class="post-meta">

            {% if site.plugins contains "jekyll/tagging" %}
            <div class="post-tags">
                {% for tag in post.tags %}
                <a class="tag" href="{{ tag | tag_url }}">{{ tag }}</a>
                {% endfor %}
            </div>
            {% endif %}
            {% if site.dash.date_format %}
              {{ post.date | date: site.dash.date_format }}
            {% else %}
              {{ post.date | date: "%b %-d, %Y" }}
            {% endif %}
            {% if site.show_excerpts == true %}
              <div class="post-excerpt">
                {{ post.content | strip_html | truncatewords: 50 }}
              </div>
            {% endif %}
          </div>
        </div>
      {% endfor %}
    </div>

    {% include pagination.html %}

    {% include tagcloud.html %}
{% else %}
<h2>no posts yet.</h2>
{% endif %}
 -->
