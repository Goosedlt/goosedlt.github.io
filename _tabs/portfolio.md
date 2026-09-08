---
layout: page
title: Portfolio
icon: fas fa-flask
order: 1
---

<div style="text-align: center; margin-bottom: 2rem;">
  <p><em>Looking for my work history, education, and qualifications?</em></p>
  <a href="/resume/" class="btn btn-primary">
    <i class="fas fa-file-alt"></i> View My Resume & Cover Letter
  </a>
</div>

<hr>

<h2 style="margin-top: 2rem; margin-bottom: 1.5rem;">Featured Projects</h2>

<div id="post-list" class="flex-grow-1 px-xl-1">
  {% assign portfolio_posts = site.posts | where: "portfolio", true %}
  {% for post in portfolio_posts %}
    <article class="card-wrapper card">
      <a href="{{ post.url | relative_url }}" class="post-preview row g-0 flex-md-row-reverse">
        <div class="col-md-12">
          <div class="card-body d-flex flex-column">
            <h1 class="card-title my-2 mt-md-0">{{ post.title }}</h1>
            <div class="card-text content mt-0 mb-3">
              <p>
                {% if post.description %}
                  {{ post.description }}
                {% else %}
                  {{ post.content | strip_html | truncatewords: 30 }}
                {% endif %}
              </p>
            </div>
            <div class="post-meta flex-grow-1 d-flex align-items-end">
              <div class="me-auto">
                <i class="far fa-calendar-alt fa-fw me-1"></i>
                <time>{{ post.date | date: "%b %d, %Y" }}</time>
              </div>
            </div>
          </div>
        </div>
      </a>
    </article>
  {% endfor %}
</div>

# Engineering Portfolio

Welcome to my featured project showcase. Below are select design, simulation, and hardware projects:

---

### [Chem E Car](/posts/Chem-E-Car/)
Thermoelectric generation powered by acid-base exothermic reactions and dry ice cooling. Awarded 1st place in regional competition.

---

### [Tequila Plant Process Simulation & Design](/posts/Tequila-Distillation/)
Rigorous simulation of distillation trains, equilibrium stages, and heat integration modeled in AVEVA Pro/II.

---

### [Sustainable Anaerobic Digester for Parks](/posts/Eco-Canine-Power/)
A sustainable, solar-powered waste station that uses anaerobic digestion to convert public dog waste into renewable energy.

---
