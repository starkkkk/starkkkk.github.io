---
layout: profile
title: "Publications"
permalink: /publications/
excerpt: "Peer-reviewed publications and ongoing doctoral research by Jiaxing Zheng."
page_class: publications
---

<header class="page-hero">
  <div class="shell">
    <p class="page-kicker">Research archive</p>
    <h1>Publications.</h1>
    <p class="page-lede">Peer-reviewed work from my Ph.D. on large language models, information diffusion, social simulation, and graph optimization.</p>
  </div>
</header>

<div class="page-content">
  <div class="shell">
    <section class="publication-group" aria-labelledby="published-heading">
      <div class="group-heading">
        <h2 id="published-heading">Published &amp; accepted</h2>
        <span>Newest first</span>
      </div>
      <ol class="publication-list">
        {% assign publication_years = site.data.publications | group_by: "year" | sort: "name" | reverse %}
        {% for year_group in publication_years %}
          {% for publication in year_group.items %}
            {% if publication.status == "published" or publication.status == "accepted" %}
              <li class="publication">
                <div class="publication__year">{{ publication.year }}</div>
                <div>
                  <h3>{{ publication.title }}</h3>
                  <p class="publication__authors">{{ publication.authors }}</p>
                  <p class="publication__venue">{{ publication.venue }}</p>
                  <p class="publication__description">{{ publication.description }}</p>
                  {% if publication.code_url %}<p class="publication__links"><a href="{{ publication.code_url }}">Code ↗</a></p>{% endif %}
                </div>
                {% if publication.url %}<a class="publication__arrow" href="{{ publication.url }}" aria-label="Open {{ publication.title }}">↗</a>{% endif %}
              </li>
            {% endif %}
          {% endfor %}
        {% endfor %}
      </ol>
    </section>

    <section class="publication-group" aria-labelledby="ongoing-heading">
      <div class="group-heading">
        <h2 id="ongoing-heading">Ongoing research</h2>
        <span>No venue claim</span>
      </div>
      <ol class="publication-list">
        {% for publication in site.data.publications %}
          {% if publication.status == "ongoing" %}
            <li class="publication">
              <div class="publication__year">Current</div>
              <div>
                <h3>{{ publication.title }}</h3>
                <p class="publication__authors">{{ publication.authors }}</p>
                <p class="publication__venue">{{ publication.venue }}</p>
                <p class="publication__description">{{ publication.description }}</p>
              </div>
            </li>
          {% endif %}
        {% endfor %}
      </ol>
    </section>
  </div>
</div>
