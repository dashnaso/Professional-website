---
layout: default
title: "Projects"
description: "Review the projects of Naso Bantubani, showcasing expertise in actuarial science, risk management, and data analysis."
permalink: /projects/
---

<section id="projects">
  <div class="container">
    <h2 data-aos="fade-up">Projects</h2>
    {% for project in site.data.projects %}
      <div class="project-item" data-aos="fade-up"> <!-- Ensure the class matches the CSS -->
        <h3>{{ project.title }}</h3>
        <p><strong>{{ project.company }}</strong>, {{ project.location }}</p>
        <p><em>{{ project.date }}</em></p>
        <p><strong>Situation:</strong> {{ project.situation }}</p>
        <p><strong>Task:</strong> {{ project.task }}</p>
        <p><strong>Action:</strong> {{ project.action }}</p>
        <p><strong>Result:</strong> {{ project.result }}</p>
        {% if project.image %}
          <img src="{{ '/assets/images/' | relative_url }}{{ project.image }}" alt="{{ project.title }}">
        {% endif %}
      </div>
    {% endfor %}
  </div>
</section>