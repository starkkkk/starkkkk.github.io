---
layout: profile
permalink: /
title: "Jiaxing Zheng — Algorithm Engineer"
excerpt: "Algorithm Engineer at ByteDance working on AI agent applications. Ph.D. from Shanghai Jiao Tong University."
page_class: home
---

<section class="hero">
  <div class="shell hero__grid">
    <div>
      <div class="availability">Based in Beijing</div>
      <p class="eyebrow">Algorithm Engineer · ByteDance</p>
      <h1>Jiaxing Zheng.</h1>
      <p class="hero__role">I develop <span>agent harnesses for real-world AI systems</span>.</p>
      <p class="hero__detail">Currently working at ByteDance in Beijing. My earlier doctoral research at Shanghai Jiao Tong University focused on social network information diffusion.</p>
      <div class="action-row">
        <a class="button button--primary" href="mailto:{{ site.author.email }}">Email me <span aria-hidden="true">↗</span></a>
        <a class="button" href="{{ base_path }}/cv/">View CV</a>
        <a class="button" href="{{ site.author.googlescholar }}">Google Scholar <span aria-hidden="true">↗</span></a>
      </div>
    </div>

    <div class="hero__portrait-wrap">
      <img class="hero__portrait" src="{{ base_path }}/images/profile-720.jpg" alt="Portrait of Jiaxing Zheng" width="686" fetchpriority="high">
      <div class="portrait-caption"><span>Jiaxing Zheng</span><span>Beijing · 2026</span></div>
    </div>
  </div>
</section>

<section class="section" aria-labelledby="experience-title">
  <div class="shell">
    <div class="section-heading">
      <div>
        <p class="section-kicker">01 · Experience</p>
        <h2 id="experience-title">Building in the real world.</h2>
      </div>
      <p>My current work centers on AI agent applications. The roles below intentionally stay at a public, non-confidential level.</p>
    </div>

    <div class="timeline">
      <article class="timeline__item">
        <div class="timeline__meta"><span>Jul 2026 — Present</span><span>Beijing, China</span></div>
        <div class="timeline__content">
          <h3>Algorithm Engineer · ByteDance</h3>
          <p>Building AI agent applications.</p>
        </div>
      </article>

      <article class="timeline__item">
        <div class="timeline__meta"><span>Apr — Jul 2025</span><span>Shanghai, China</span></div>
        <div class="timeline__content">
          <h3>Algorithm Engineer Intern · ByteDance</h3>
          <p>Worked on AIGC and recommendation-related applications.</p>
        </div>
      </article>
    </div>
  </div>
</section>

<section class="section" aria-labelledby="research-title">
  <div class="shell">
    <div class="section-heading">
      <div>
        <p class="section-kicker">02 · Ph.D. Research</p>
        <h2 id="research-title">Information diffusion at scale.</h2>
      </div>
      <p>During my Ph.D., I studied how information spreads through social networks: how to predict it early, simulate it efficiently, and optimize interventions.</p>
    </div>

    <div class="research-grid">
      {% assign selected_index = 0 %}
      {% for publication in site.data.publications %}
        {% if publication.selected %}
          {% assign selected_index = selected_index | plus: 1 %}
          <article class="research-card">
            <span class="research-card__number">0{{ selected_index }}</span>
            <h3>{{ publication.project }}</h3>
            <p>{{ publication.description }}</p>
            <p class="research-card__result">{{ publication.result }}</p>
            {% if publication.url %}
              <a class="research-card__link" href="{{ publication.url }}">Read paper <span aria-hidden="true">↗</span></a>
            {% endif %}
          </article>
        {% endif %}
      {% endfor %}
    </div>

    <div class="action-row">
      <a class="button" href="{{ base_path }}/publications/">All publications</a>
    </div>
  </div>
</section>

<section class="section" aria-labelledby="education-title">
  <div class="shell">
    <div class="section-heading">
      <div>
        <p class="section-kicker">03 · Education</p>
        <h2 id="education-title">Shanghai Jiao Tong University.</h2>
      </div>
      <p>My doctoral training combined large language models, graph learning, reinforcement learning, and social computing.</p>
    </div>

    <div class="education-grid">
      <article class="education-card">
        <span class="education-card__date">2021 — 2026</span>
        <h3>Ph.D. · School of Computer Science</h3>
        <p>Shanghai Jiao Tong University</p>
      </article>
      <article class="education-card">
        <span class="education-card__date">2017 — 2021</span>
        <h3>B.S. · School of Cyber Science and Engineering</h3>
        <p>Shanghai Jiao Tong University</p>
      </article>
    </div>
  </div>
</section>

<section class="section" aria-labelledby="contact-title">
  <div class="shell">
    <div class="contact-panel">
      <div>
        <p class="section-kicker">04 · Contact</p>
        <h2 id="contact-title">Let’s talk about agents, research, or something worth building.</h2>
        <p>The best way to reach me is by email.</p>
      </div>
      <div class="contact-panel__links">
        <a href="mailto:{{ site.author.email }}"><span>Email</span><span aria-hidden="true">↗</span></a>
        <a href="https://github.com/starkkkk"><span>GitHub</span><span aria-hidden="true">↗</span></a>
        <a href="{{ site.author.googlescholar }}"><span>Google Scholar</span><span aria-hidden="true">↗</span></a>
      </div>
    </div>
  </div>
</section>
