---
layout: default
title: About
permalink: /about/
---

# About

I work on systems where clarity, reliability, and trust matter.

---

## What I Do

I align people, process, and data so organisations can make better decisions and deliver change without unnecessary friction.

In practice, that often means simplifying reporting, strengthening ownership, and introducing automation in a way teams can understand — and rely on.

---

## Where I Work Best

I’m most interested in work that sits between strategy and execution.

The gap is usually not intent.

It’s translation: turning decisions into systems that hold up under real operational pressure.

---

## What I Optimise For

- **Clear ownership and accountability**  
- **Decision-focused reporting**  
- **Sustainable automation**  
- **Change that teams actually adopt**  

---

## This Site

This site captures examples of that work, along with short notes on what I’ve learned along the way.

If you’re new here, the best entry points are usually the Thinking posts.

---


<h2>Latest Thinking</h2>

{% assign latest_thinking = site.categories.Thinking | sort: "date" | reverse | slice: 0,3 %}

{% if latest_thinking.size > 0 %}
{% for post in latest_thinking %}
<article class="post-card">
<h3 class="post-title">
<a href="{{ post.url }}">{{ post.title }}</a>
</h3>
  
<div class="post-meta muted">
{{ post.date | date: "%-d %b %Y" }}
</div>

{% if post.excerpt %}
<p class="post-excerpt">
{{ post.excerpt | strip_html }}
</p>
{% endif %}

<a class="post-readmore muted" href="{{ post.url }}">Read →</a>
</article>

{% unless forloop.last %}
<div style="height:1.75rem"></div>
{% endunless %}
{% endfor %}
{% endif %}
