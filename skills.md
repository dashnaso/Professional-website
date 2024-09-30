---
layout: default
title: "Skills"
description: "Discover the key skills and expertise of Naso Bantubani in actuarial science, risk management, and data analysis."
permalink: /skills/
---

<section id="skills">
  <div class="container">
    <h2 data-aos="fade-up">Key Skills & Expertise</h2>
    {% for category in site.data.skills %}
      <h3 data-aos="fade-right">{{ category.category }}</h3>
      {% for skill in category.skills %}
        <div class="skill-item" data-aos="fade-up">
          <h4>{{ skill.name }}</h4>
          <p><strong>Key Strengths:</strong></p>
          <ul>
            {% for strength in skill.strengths %}
              <li>{{ strength }}</li>
            {% endfor %}
          </ul>
          {% if skill.proficient_in %}
          <p><strong>Proficient In:</strong></p>
          <ul>
            {% for prof in skill.proficient_in %}
              <li>{{ prof }}</li>
            {% endfor %}
          </ul>
          {% endif %}
          <p><strong>Notable Achievements:</strong></p>
          {% for achievement in skill.achievements %}
            <p><em>{{ achievement.title }}</em></p>
            {% if achievement.situation %}
            <ul>
              <li><strong>Situation:</strong> {{ achievement.situation }}</li>
              <li><strong>Action:</strong> {{ achievement.action }}</li>
              <li><strong>Result:</strong> {{ achievement.result }}</li>
            </ul>
            {% else %}
            <p>{{ achievement.description }}</p>
            {% endif %}
          {% endfor %}
        </div>
      {% endfor %}
    {% endfor %}
  </div>
</section>
