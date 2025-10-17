---
layout: single
author_profile: true
---

Hi, I'm Scott Watson 👋

Aerospace Engineer \| Experimental Combustion \| Data Analysis

---

Thanks for stopping by! I'm am an aerospace engineer with a keen interest in everything design and engineering related.
I'm expanding my horizons and eager to apply my skills in new design and analysis roles, where my experience can be best used.

## Professional Timeline 📅

<div class="grid-main">
  <section id="timeline">
    <!-- <div class="timeline-year">
        <span>Present</span>
    </div> -->
    {% assign sorted_coops = site.coops | sort: 'start_date' | reverse %}
    {% assign current_year = '' %}
    <ul class="timeline-list">
      {% for coop in sorted_coops %}
        {% assign coop_year = coop.end_date | date: "%Y" %}
        {% if coop_year != current_year %}
            <li class="timeline-year">
                <span>{{ coop_year }}</span>
            </li>
            {% assign current_year = coop_year %}
        {% endif %}
        <li class="timeline-item {% cycle 'left', 'right' %}" 
            data-type="{{ coop.tags | first }}"
            data-aos="{% cycle 'fade-right', 'fade-left' %}">
          <div class="timeline-dot"></div>
          <div class="timeline-content">
            {% if coop.logo %}
                <img src="{{ coop.logo | relative_url }}" alt="{{ coop.title }} logo" class="timeline-logo">
            {% endif %}
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


