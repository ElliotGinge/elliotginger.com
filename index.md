---
layout: default
title:
permalink: /
---

# Elliot Ginger

<span class="muted" style="letter-spacing:.18em;text-transform:uppercase;">
Systems • Data • Automation
</span>

<div style="height:2rem"></div>

I design clarity in systems — aligning people, process, and data so decisions become easier and delivery becomes faster.

<div style="height:1rem"></div>

I turn fragmented reporting, manual processes, and unclear ownership into coherent systems teams can trust.

<div style="height:2rem"></div>

## What you’ll find here

- **Work** — outcome-focused case studies showing how systems and reporting were improved in practice  
- **Thinking** — short notes on analytics, automation, governance, and change that sticks  
- **About** — how I work, what I optimise for, and the trade-offs I care about  

<div style="height:2rem"></div>

## Start Here

<div style="height:2.5rem"></div>

## Latest Thinking

{% assign latest_thinking = site.categories.Thinking | sort: "date" | reverse | slice: 0,3 %}

{% if latest_thinking.size > 0 %}
<div class="posts-preview">
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
</div>

<div style="height:1rem"></div>

<a class="muted" href="/thinking/">View all Thinking posts →</a>

{% endif %}

<div style="height:2rem"></div>

<span class="muted">
This is a living body of work. New case studies and notes are added regularly.
</span>
