---
layout: default
title: Thinking
permalink: /thinking/
---

# Thinking

Short notes on systems, analytics, automation, governance, and change that sticks.

<div style="height:1.5rem"></div>

{% if site.posts.size == 0 %}
<span class="muted">No posts yet.</span>
{% else %}

{% for post in site.posts %}
<article class="post-card">
  <h2 class="post-title">
    <a href="{{ post.url }}">{{ post.title }}</a>
  </h2>

  <div class="post-meta muted">
    {{ post.date | date: "%-d %b %Y" }}
  </div>

  {% if post.excerpt %}
  <p class="post-excerpt">
    {{ post.excerpt | strip_html | truncate: 220 }}
  </p>
  {% endif %}

  <a class="post-readmore muted" href="{{ post.url }}">Read →</a>
</article>
{% endfor %}

{% endif %}
