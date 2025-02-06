---
layout: default
title: "My Foam Blog"
---

# My Foam Blog

Welcome to my blog. Below are my latest posts.

{% for post in paginator.posts %}
## [{{ post.title }}]({{ post.url | relative_url }})
*Published on {{ post.date | date: "%B %d, %Y" }}*

{{ post.excerpt }}

{% endfor %}

{% if paginator.total_pages > 1 %}
<div class="pagination">
  {% if paginator.previous_page %}
    <a href="{{ paginator.previous_page_path | relative_url }}">&laquo; Newer Posts</a>
  {% endif %}
  {% if paginator.next_page %}
    <a href="{{ paginator.next_page_path | relative_url }}">Older Posts &raquo;</a>
  {% endif %}
</div>
{% endif %}
