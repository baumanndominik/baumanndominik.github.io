---
layout: single
title: "Cyber-physical Systems Group"
permalink: /research_group/
author_profile: true
---

I am leading the [Cyber-physical Systems Group](https://www.aalto.fi/en/department-of-electrical-engineering-and-automation/cyber-physical-systems) at Aalto University.

## Team

{% assign active = site.data.members | where: "status", "active" %}
{% assign postdocs = active | where: "type", "postdoc" %}
{% assign phds = active | where: "type", "phd" %}
{% assign ordered = postdocs | concat: phds %}

<div class="two-col">
  <div class="col">
    {% for m in ordered %}
      {% assign parity = forloop.index0 | modulo: 2 %}
      {% if parity == 0 %}
      <p><a href="{{ m.url }}">{{ m.name }}</a><br><sup>{{ m.role }}</sup></p>
      {% endif %}
    {% endfor %}
  </div>
  <div class="col">
    {% for m in ordered %}
      {% assign parity = forloop.index0 | modulo: 2 %}
      {% if parity == 1 %}
      <p><a href="{{ m.url }}">{{ m.name }}</a><br><sup>{{ m.role }}</sup></p>
      {% endif %}
    {% endfor %}
  </div>
</div>

## Alumni

{% assign alumni = site.data.members | where: "status", "alumni" %}
{% assign alumni_postdocs = alumni | where: "type", "postdoc" %}
{% assign alumni_phds = alumni | where: "type", "phd" %}
{% assign alumni_ordered = alumni_postdocs | concat: alumni_phds %}

<div class="two-col">
  <div class="col">
    {% for m in alumni_ordered %}
      {% assign parity = forloop.index0 | modulo: 2 %}
      {% if parity == 0 %}
      <p><a href="{{ m.url }}">{{ m.name }}</a><br><sup>{{ m.role }}</sup></p>
      {% endif %}
    {% endfor %}
  </div>
  <div class="col">
    {% for m in alumni_ordered %}
      {% assign parity = forloop.index0 | modulo: 2 %}
      {% if parity == 1 %}
      <p><a href="{{ m.url }}">{{ m.name }}</a><br><sup>{{ m.role }}</sup></p>
      {% endif %}
    {% endfor %}
  </div>
</div>

