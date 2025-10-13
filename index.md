---
layout: single
author_profile: true
---

👋 Hi, I'm Scott Watson

Aerospace Engineer | Experimental Combustion | Data Analysis

Thanks for stopping by! I'm am an aerospace engineer with a keen interest in everything space related.
I'm interested in expanding my horizons and applying my skills in new fields.

## Professional Timeline

<div class="grid-main">
  <section id="timeline">
    <ul class="timeline-list">
      {% assign sorted_coops = site.coops | sort: 'date' | reverse %}
      {% for coop in sorted_coops %}
        <li class="timeline-item {% cycle 'left', 'right' %}" 
            data-type="{{ coop.tags | first }}"
            data-aos="{% cycle 'fade-right', 'fade-left' %}">
          <div class="timeline-dot"></div>
          <div class="timeline-content">
            <a href="{{ coop.url }}">{{ coop.title }}</a>
            {% if coop.position %}
              <h4 class="timeline-position">{{ coop.position }}</h4>
            {% endif %}
            <span class="timeline-date">
              {{ coop.start_date | date: "%b %Y" }}
              –
              {% if coop.end_date %}
                {{ coop.end_date | date: "%b %Y" }}
              {% else %}
                Present
              {% endif %}
            </span>
            <p>{{ coop.excerpt }}</p>
          </div>
        </li>
      {% endfor %}
    </ul>
  </section>
</div>


