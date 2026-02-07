---
layout: default
title: The Ginger Arms Ordering System
permalink: /work/ginger-arms-ordering-system/
---

## Context

I built a lightweight ordering system for my home bar project, The Ginger Arms — not as a technical exercise, but to improve the guest experience and reduce friction while hosting.

The aim was to create something that felt like a real venue experience, without introducing complexity or ongoing maintenance overhead.

![Guest-facing ordering interface for The Ginger Arms](/assets/images/ginger-arms/ordering-interface.png)

<span class="muted">
Guest-facing ordering interface — designed to reduce friction while hosting.
</span>

## The Problem

As the space and menu evolved, the informal approach to ordering started to break down:

- Orders were easy to mishear or forget during conversation
- Menu options expanded beyond what was practical to explain repeatedly
- Availability and specials weren’t always clear
- The experience felt less polished than the space itself

The challenge was to improve consistency and clarity without making the experience feel transactional or over-engineered.

## The Approach

I approached it as a small product, with delivery constraints baked in.

### Product & UX
- Designed a simple, linear journey: browse → customise → confirm
- Made the system intuitive enough for first-time users with no explanation
- Kept the focus on speed and clarity over feature depth
- Ensured the experience complemented hosting rather than replacing it

### Engineering & Delivery
- Built a single source of truth for menus, options, and availability
- Designed the system to fail safely, with manual fallback always possible
- Kept the architecture intentionally lightweight to reduce operational risk
- Prioritised easy deployment and low ongoing maintenance
- The system was implemented as a small web application with a simple data store, designed for reliability over scale.

Features were introduced incrementally, with each change validated in real use rather than speculative design.

<img src="/assets/images/ginger-arms/admin-control.png"
     alt="Admin controls for managing orders and bar availability"
     class="shot shot-admin">

<span class="muted">
Admin controls for managing orders and bar availability during service.
</span>


<span class="muted">
Admin interface for on-the-fly menu changes and order management
</span>


## The Outcome

The system delivered practical benefits on both sides of the experience:

- Guests found ordering clearer and more enjoyable
- Hosting became less interrupt-driven and easier to manage
- Menu changes and specials were simpler to keep up to date
- The overall experience felt more intentional and “venue-like”

The result was a small system that improved flow and enjoyment, without becoming something that needed constant attention.

## Key Takeaways

- Product thinking applies at any scale
- UX and reliability matter more than features
- Lightweight systems often deliver the highest return
- Delivery choices should reflect how something will actually be used
