---
layout: default
title: "Experience"
description: "Review the professional experience of Naso Bantubani, highlighting roles and responsibilities in actuarial science and risk management."
permalink: /experience/
---

<section id="experience">
  <div class="container">
    <h2 data-aos="fade-up">Professional Experience</h2>
    
    {% for job in site.data.experience.jobs %}
      <div class="job-item" data-aos="fade-up">
        <h3>{{ job.position }}</h3>
        <p><strong>{{ job.company }}</strong>, {{ job.location }}</p>
        <p><em>{{ job.date }}</em></p>
        <ul>
          {% for responsibility in job.responsibilities %}
            <li>{{ responsibility }}</li>
          {% endfor %}
        </ul>
      </div>
    {% endfor %}
    
    <h3 data-aos="fade-up">Key Achievements</h3>
    
    {% for achievement in site.data.experience.key_achievements %}
      <div class="achievement-item" data-aos="fade-up">
        <p>{{ achievement }}</p>
      </div>
    {% endfor %}
    
  </div>
</section>