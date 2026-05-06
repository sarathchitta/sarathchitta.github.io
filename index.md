---
layout: default
title: Venkata Sarath Chitta
---

## About Me

<div class="about-hero">
  <div class="about-hero-image-wrap">
    <div
      class="about-hero-image"
      role="img"
      aria-label="Professional headshot of Venkata Sarath Chitta"
    >VC</div>
  </div>
  <div class="about-hero-content">
    <p>I am a curious builder with a strong growth mindset. I believe people can continuously reinvent themselves through learning, exploration, and deliberate experimentation. I enjoy diving into new domains, connecting ideas across disciplines, and building from first principles.</p>

    <p>Recently, I’ve been spending more time in the research space — exploring long-form thinking, experimentation loops, autonomous systems, distributed training, GPU systems, and large-scale inference infrastructure. I’m especially interested in how intelligent systems and scalable compute can accelerate human creativity, research, and decision-making.</p>

    <p>As a hands-on Principal Software Engineer, I specialize in building ultra-scalable, low-latency, cloud-native platforms and AI-powered systems from the ground up. My work spans distributed systems internals, agentic workflows, AI orchestration, and hyperscale infrastructure.</p>

    <p>Throughout my career, I’ve often been trusted with high-risk, ambiguous, early-stage initiatives — projects without clear playbooks, established markets, or proven paths. I thrive in zero-to-one environments, operating with a fail-fast, user-feedback-driven mindset to rapidly iterate toward product-market fit.</p>

    <p>I’ve led and shipped systems delivering $100M+ business impact, scaled platforms handling 100K+ TPS, and contributed production code across the full stack. Along the way, I’ve learned that strong conviction, speed of learning, and relentless execution matter more than perfect ideas.</p>

    <p>📍 Seattle, WA, USA &nbsp;|&nbsp; ✉️ <a href="mailto:sarath.chitta@gmail.com">sarath.chitta@gmail.com</a> &nbsp;|&nbsp; <a href="https://linkedin.com/in/sarath-chitta">LinkedIn</a> &nbsp;·&nbsp; <a href="/projects/">Projects</a></p>
  </div>
</div>

---

## Core Expertise

| Domain | Details |
|--------|---------|
| **Distributed Systems** | Architecture & Scalability (100K+ TPS, sub-millisecond latency) |
| **AI & Agentic Systems** | Multimodal AI, Copilot integrations, AI Orchestration, RAG, Deep Learning |
| **Cloud Platforms** | Azure, AWS — hyperscale cloud architecture |
| **Event-Driven Architecture** | Streaming architectures, real-time data pipelines |
| **High-Performance Systems** | Low-latency design, memory optimization, throughput scaling |
| **Hands-on Engineering** | Full-stack implementation, code reviews, prototyping, mentoring |
| **Coding** | C#, Java, C++, Python, TypeScript, Android, React, Rust

---

## Professional Experience

### Microsoft — Principal Software Engineer
📍 Redmond, WA &nbsp;·&nbsp; 🗓 2017 – Present

- Built and scaled **Microsoft Teams Events** chat platform end-to-end, driving ~**$100M** business impact
- Implemented multimodal AI integration enabling **Copilot** to understand shared screen content (**Visual Insights**); improved customer satisfaction by 15%, optimized GPU consumption by 4×
- Built extensible AI-driven **Search Insights** platform across Microsoft Exchange ecosystem — hands-on with indexing, ranking, and serving layers
- Engineered cloud buildout automation reducing deployment time from **6 months to 2 months**
- Built and optimized **Exchange Admin Management APIs** handling ~2M requests/day and scaled existing system to handle ~500K (from 100K) objects in a single tenant

### CreativeCubs — Founder & Architect
📍 India &nbsp;·&nbsp; 🗓 2016 – 2017

- Built Android application with **300K+ monthly active users**
- Implemented scalable backend and ML-based gold price forecasting system
- Owned full product lifecycle — wrote core backend services, built ML pipelines, and scaled systems hands-on

### Amazon — Software Development Engineer / Architect
📍 India &nbsp;·&nbsp; 🗓 2012 – 2016

- Scaled vendor payments invoice-matching platform to handle **5× load**; reduced processing time by 90%
- Increased throughput from 100 req/sec to **800 req/sec** while reducing tp99 latency from 500ms to 100ms
- Built anomaly detection and self-healing invoice processing pipeline

### D. E. Shaw & Co. — Senior Developer / Project Leader
📍 India &nbsp;·&nbsp; 🗓 2006 – 2012

- Reduced trading order placement latency from **1800µs to 800µs** using lock-free data structures and OS/hardware-interface optimizations
- Built transactional persistence framework handling **100K TPS**
- Scaled trading universe from 5K to **100K instruments**
- Implemented lock-free queues, concurrent hash maps, memory-mapped I/O, and memory optimization reclaiming 70–80% runtime objects

---

## Education

🎓 **MS, Computer Science** — Computational Perception & Robotics
*Georgia Institute of Technology*

🎓 **B.Tech, Computer Science**
*Andhra University, India*

---

<p align="center">
  <a href="/projects/">➡️ <strong>View All Projects</strong></a>
</p>

---

## Latest Posts

{% assign recent_posts = site.posts | slice: 0, 3 %}
{% if recent_posts.size > 0 %}
<ul class="latest-posts latest-posts-compact">
  {% for post in recent_posts %}
  <li class="latest-post-item">
    <a href="{{ post.url | relative_url }}"><strong>{{ post.title }}</strong></a>
    <span class="latest-post-meta">{{ post.date | date: "%B %-d, %Y" }}</span>
  </li>
  {% endfor %}
</ul>
{% else %}
<p class="latest-posts-empty">No posts published yet. First article coming soon.</p>
{% endif %}

<p><a href="{{ '/blog/' | relative_url }}">Read the blog archive →</a></p>
