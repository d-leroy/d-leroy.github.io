---
layout: page
permalink: /cv/
title: CV
description: # my CV.
nav: true
---

{% assign degrees = site.data.cv.degrees %}
{% if degrees %}
<section class="section experiences-section">
  <h2 class="section-title">
    Education
  </h2>

  {% for degree in degrees %}
  <div class="item">

    <div class="meta">

      <div class="upper-row">
        <h3 class="job-title">{{ degree.degree }}</h3>
        <div class="time">{{ degree.time }}</div>
      </div><!--//upper-row-->

      <div class="company">{{ degree.university }}</div>

    </div><!--//meta-->

    {% if degree.details %}
    <div class="details">
      {{ degree.details | markdownify }}
    </div><!--//details-->
    {% endif %}

  </div><!--//item-->
  {% endfor %}

</section><!--//section-->
{% endif %}

{% assign internships = site.data.cv.internships %}
{% if internships %}
<section class="section experiences-section">
  <h2 class="section-title">
    Internships
  </h2>

  {% for internship in internships %}
  <div class="item">

    <div class="meta">

      <div class="upper-row">
        <h3 class="job-title">{{ internship.subject }}</h3>
        <div class="time">{{ internship.time }}</div>
      </div><!--//upper-row-->

      <div class="company">{{ internship.company }}</div>

    </div><!--//meta-->

    {% if internship.details %}
    <div class="details">
      {{ internship.details | markdownify }}
    </div><!--//details-->
    {% endif %}

  </div><!--//item-->
  {% endfor %}

</section><!--//section-->
{% endif %}

{% assign experiences = site.data.cv.experiences %}
{% if experiences %}
<section class="section experiences-section">
  <h2 class="section-title">
    Experiences
  </h2>

  {% for experience in experiences %}
  <div class="item">

    <div class="meta">

      <div class="upper-row">
        <h3 class="job-title">{{ experience.role }}</h3>
        <div class="time">{{ experience.time }}</div>
      </div><!--//upper-row-->

      <div class="company">{{ experience.company }}</div>

    </div><!--//meta-->

    {% if experience.details %}
    <div class="details">
      {{ experience.details | markdownify }}
    </div><!--//details-->
    {% endif %}

  </div><!--//item-->
  {% endfor %}

</section><!--//section-->
{% endif %}

