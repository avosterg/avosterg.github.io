---
layout: default
title: Home
---

<div class="posts">
  {% for post in site.posts %}
    <article class="post">
      <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
      <p class="post-date">{{ post.date | date: "%B %d, %Y" }}</p>
      <div class="post-excerpt">
        {{ post.excerpt }}
      </div>
      <a href="{{ post.url }}" class="read-more">Read More →</a>
    </article>
  {% endfor %}
</div>

{% if site.posts.size == 0 %}
  <p>No posts yet. Create your first post in the <code>_posts</code> folder!</p>
{% endif %}
