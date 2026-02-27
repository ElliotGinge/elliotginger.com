---
layout: default
title: Thinking
permalink: /thinking/
---

# Thinking

Short notes on systems, analytics, automation, governance, and change that sticks.

<span class="muted">
Technology doesn’t create clarity. Structure does.
</span>

<div style="height:1.25rem"></div>

{% assign thinking_posts = site.categories.Thinking | sort: "date" | reverse %}

{% assign all_tags_csv = "" %}
{% for post in thinking_posts %}
  {% if post.tags %}
    {% assign all_tags_csv = all_tags_csv | append: post.tags | join: "," | append: "," %}
  {% endif %}
{% endfor %}
{% assign all_tags = all_tags_csv | split: "," | uniq | sort %}
{% assign all_tags = all_tags | where_exp: "t", "t != ''" %}

{% if all_tags.size > 0 %}
<div class="tagbar" id="tagbar" aria-label="Filter posts by tag">
  <button class="tag active" data-tag="all" type="button">All</button>
  {% for tag_name in all_tags %}
    <button class="tag" data-tag="{{ tag_name | escape }}" type="button">{{ tag_name }}</button>
  {% endfor %}
</div>
{% endif %}

<div style="height:1.5rem"></div>

{% if thinking_posts.size == 0 %}
<span class="muted">No posts yet.</span>
{% else %}

<div id="posts">
{% for post in thinking_posts %}
  {% assign post_tags = post.tags | join: "," %}
  <article class="post-card" data-tags="{{ post_tags | escape }}">
    <h2 class="post-title">
      <a href="{{ post.url }}">{{ post.title }}</a>
    </h2>

    <div class="post-meta muted">
      {{ post.date | date: "%-d %b %Y" }}
      {% if post.tags and post.tags.size > 0 %}
        <span class="dot">•</span>
        <span class="post-tags">
          {% for t in post.tags %}
            <span class="post-tag">{{ t }}</span>{% unless forloop.last %}<span class="dot">•</span>{% endunless %}
          {% endfor %}
        </span>
      {% endif %}
    </div>

    {% if post.excerpt %}
      <p class="post-excerpt">
        {{ post.excerpt | strip_html }}
      </p>
    {% endif %}

    <a class="post-readmore muted" href="{{ post.url }}">Read →</a>
  </article>
{% endfor %}
</div>

<div class="muted" id="noResults" style="display:none; margin-top:1rem;">
  No posts match that tag.
</div>

<script>
  (function () {
    const tagbar = document.getElementById('tagbar');
    const postsWrap = document.getElementById('posts');
    const noResults = document.getElementById('noResults');

    if (!tagbar || !postsWrap) return;

    const buttons = Array.from(tagbar.querySelectorAll('button[data-tag]'));
    const posts = Array.from(postsWrap.querySelectorAll('.post-card'));

    function setActive(btn) {
      buttons.forEach(b => b.classList.toggle('active', b === btn));
    }

    function filter(tag) {
      let shown = 0;

      posts.forEach(p => {
        const tags = (p.getAttribute('data-tags') || '')
          .split(',')
          .map(s => s.trim())
          .filter(Boolean);

        const ok = (tag === 'all') || tags.includes(tag);
        p.style.display = ok ? '' : 'none';
        if (ok) shown++;
      });

      if (noResults) noResults.style.display = shown === 0 ? '' : 'none';
    }

    tagbar.addEventListener('click', (e) => {
      const btn = e.target.closest('button[data-tag]');
      if (!btn) return;

      const tag = btn.getAttribute('data-tag');
      setActive(btn);
      filter(tag);

      if (tag === 'all') {
        history.replaceState(null, '', window.location.pathname);
      } else {
        history.replaceState(null, '', window.location.pathname + '#' + encodeURIComponent(tag));
      }
    });

    const initial = decodeURIComponent((window.location.hash || '').replace('#', '')) || 'all';
    const initialBtn = buttons.find(b => b.getAttribute('data-tag') === initial) || buttons[0];
    setActive(initialBtn);
    filter(initial);
  })();
</script>

{% endif %}
