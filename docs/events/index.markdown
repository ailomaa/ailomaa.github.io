---
title: Events
layout: default
---

{% assign events = site.events | sort: "date" | reverse %}
{% capture now %}
  {{'now' | date: '%s'}}
{% endcapture %}

<h2>Upcoming Events</h2>
{% for event in events %}
  {% capture event_date %}
    {{event.date | date: '%s'}}
  {% endcapture %}
  {% if event_date >= now %}
  <div class="event-list-row">
    <a href="{{ event.url }}">
      <div class="event-content">
        <h3><span class="event-type">{{ event.type }}:</span> {{ event.title }}</h3>
        <p><b>Presenters:</b> {{ event.presenters }}</p>
        <p><b>Date:</b> {{ event.date | date: "%-d %B, %Y" }}</p>
        <p><b>Time:</b> {{ event.date | date:  "%H:%M" }}</p>
        <p><b>Where:</b> {{ event.location }}</p>
      </div>
    </a>
  </div>
  {% endif %}
{% endfor %}


<h2>Past Events</h2>
{% for event in events %}
  {% capture event_date %}
    {{event.date | date: '%s'}}
  {% endcapture %}
  {% if event_date < now %}
  <div class="event-list-row">
    <a href="{{ event.url }}">
      <div class="event-content">
        <h3><span class="event-type">{{ event.type }}:</span> {{ event.title }}</h3>
        <p><b>Presenters:</b> {{ event.presenters }}</p>
        <p><b>Date:</b> {{ event.date | date: "%-d %B, %Y"}}</p>
        <p><b>Time:</b> {{ event.date | date:  "%H:%M" }}</p>
        <p><b>Where:</b> {{ event.location }}</p>
      </div>
    </a>
  </div>
  {% endif %}
{% endfor %}
