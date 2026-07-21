## Team

{% assign active = site.data.members | where: "status", "active" %}
{% assign postdocs = active | where: "type", "postdoc" %}
{% assign phds = active | where: "type", "phd" %}
{% assign ordered = postdocs | concat: phds %}

<div class="two-col">
  <div class="col">
    {% for m in ordered %}
      {% if forloop.index0 | modulo: 2 == 0 %}
      <p>
        <a href="{{ m.url }}">{{ m.name }}</a><br>
        <sup>{{ m.role }}</sup>
      </p>
      {% endif %}
    {% endfor %}
  </div>
  <div class="col">
    {% for m in ordered %}
      {% if forloop.index0 | modulo: 2 == 1 %}
      <p>
        <a href="{{ m.url }}">{{ m.name }}</a><br>
        <sup>{{ m.role }}</sup>
      </p>
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
      {% if forloop.index0 | modulo: 2 == 0 %}
      <p>
        <a href="{{ m.url }}">{{ m.name }}</a><br>
        <sup>{{ m.role }}</sup>
      </p>
      {% endif %}
    {% endfor %}
  </div>
  <div class="col">
    {% for m in alumni_ordered %}
      {% if forloop.index0 | modulo: 2 == 1 %}
      <p>
        <a href="{{ m.url }}">{{ m.name }}</a><br>
        <sup>{{ m.role }}</sup>
      </p>
      {% endif %}
    {% endfor %}
  </div>
</div>

