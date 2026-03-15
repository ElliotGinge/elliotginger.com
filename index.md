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

Much of my work sits where reporting, operations, and technology meet.  
I turn fragmented reporting, manual processes, and unclear ownership into coherent systems teams can trust.

<div style="height:2rem"></div>

This site is where I share the thinking behind that work — along with practical examples of how systems and reporting can be improved in the real world.

<div style="height:2rem"></div>

## What you’ll find here

- **Work** — outcome-focused case studies showing how systems and reporting were improved in practice  
- **Thinking** — short notes on analytics, automation, governance, and change that sticks  
- **About** — how I work, what I optimise for, and the trade-offs I care about  

<div style="height:2.5rem"></div>

## Selected Work

A few examples of systems work and practical improvements delivered in real environments.

<div class="posts-preview">

<article class="post-card">
  <h3 class="post-title">
    <a href="/work/when-metrics-mean-different-things/">When Metrics Mean Different Things</a>
  </h3>

  <p class="post-excerpt">
    Restoring decision velocity by aligning conflicting definitions and rebuilding trust in reporting.
  </p>

  <a class="post-readmore muted" href="/work/when-metrics-mean-different-things/">View case study →</a>
</article>

<div style="height:1.75rem"></div>

<article class="post-card">
  <h3 class="post-title">
    <a href="/work/automation-with-control/">Automation with Control</a>
  </h3>

  <p class="post-excerpt">
    Reducing manual operational effort through controlled automation while maintaining visibility and trust.
  </p>

  <a class="post-readmore muted" href="/work/automation-with-control/">View case study →</a>
</article>

</div>

<div style="height:0.75rem"></div>

<a class="muted" href="/work/">View all work →</a>

<div style="height:2rem"></div>

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
This is a living body of work. New case studies and notes are added over time.
</span>
