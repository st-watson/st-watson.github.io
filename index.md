---
layout: single
author_profile: true
---

👋 Hi, I'm Scott Watson

Aerospace Engineer | Experimental Combustion | Data Analysis

## Professional Timeline

<!-- <ul class="timeline">
    {% for entry in site.data.timeline %}
        <li>
            <time>{{ entry.date | date: "%b %Y" }} – {{ entry.end_date | date: "%b %Y" }}</time>
            <h3><a href="{{ entry.link | relative_url }}">{{ entry.title }}</a></h3>
            <p>{{ entry.description }}</p>
        </li>
    {% endfor %} -->

<section id="timeline">
  <ul class="timeline-list">
    {% assign sorted_coops = site.coops | sort: 'date' | reverse %}
    {% for coop in sorted_coops %}
      <li class="timeline-item {% if forloop.index0 | modulo:2 == 0 %}left{% else %}right{% endif %}" 
            data-type="{{ coop.tags | first }}"
            data-aos="{% if forloop.index0 | modulo:2 == 0 %}fade-right{% else %}fade-left{% endif %}">
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
