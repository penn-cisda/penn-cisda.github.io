---
layout: page
title: People
---
<style type="text/css">
    .people {
        display: grid;
        grid-template-columns: repeat(4, minmax(0, 1fr));
        gap: 1rem;
        text-align: center;
    }
    .people figure {
        margin: 0;
    }
    .people img {
        max-width: 100%;
    }
    @media (max-width: 700px) {
        .people {
            grid-template-columns: repeat(2, minmax(0, 1fr));
        }
    }
    @media (max-width: 400px) {
        .people {
            grid-template-columns: 1fr;
        }
    }
</style>

<h1>Current CISDA Members</h1>
<div class="people">
    {% for person in site.data.people %}
      {% if person.status == "current" %}
        {% include person.html name=person.name img=person.img url=person.url position=person.position position2=person.position2 %}
      {% endif %}
    {% endfor %}
</div>

<h1>Former CISDA Members</h1>
<div class="people">
    {% for person in site.data.people %}
      {% if person.status == "former" %}
        {% include person.html name=person.name img=person.img url=person.url position=person.position position2=person.position2 %}
      {% endif %}
    {% endfor %}
</div>
