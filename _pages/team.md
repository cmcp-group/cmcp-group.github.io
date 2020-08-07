---
title: "Computational Materials and Chemical Processes Lab - Members"
layout: gridlay
excerpt: "Computational Materials and Chemical Processes Lab - Members"
sitemap: false
permalink: /team/
---

# Group Members

 **We are looking for new PhD students, Postdocs, and Master students to join the team** [(see openings)]({{ site.url }}{{ site.baseurl }}/vacancies) **!**

Jump to [members](#Members), and [alumni](#alumni).

## Principal Investigator

{% for member in site.data.pi %}

<div class="row">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h3>{{ member.name }}</h3>
  <b><i style="font-size:18px">{{ member.info }}</i></b><br>

  {% if member.scholar %} <a href="{{ member.scholar }}"><i class="ai ai-google-scholar-square ai-3x"></i></a> {% endif %}

  {% if member.number_educ == 1 %}
    <li> {{ member.education1 }} </li>
    {% endif %}

    {% if member.number_educ == 2 %}
    <li> {{ member.education1 }} </li>
    <li> {{ member.education2 }} </li>
    {% endif %}

    {% if member.number_educ == 3 %}
    <li> {{ member.education1 }} </li>
    <li> {{ member.education2 }} </li>
    <li> {{ member.education3 }} </li>
    {% endif %}

    {% if member.number_educ == 4 %}
    <li> {{ member.education1 }} </li>
    <li> {{ member.education2 }} </li>
    <li> {{ member.education3 }} </li>
    <li> {{ member.education4 }} </li>
    {% endif %}

    {% if member.number_educ == 5 %}
    <li> {{ member.education1 }} </li>
    <li> {{ member.education2 }} </li>
    <li> {{ member.education3 }} </li>
    <li> {{ member.education4 }} </li>
    <li> {{ member.education5 }} </li>
    {% endif %}

    {% if member.number_educ == 6 %}
    <li> {{ member.education1 }} </li>
    <li> {{ member.education2 }} </li>
    <li> {{ member.education3 }} </li>
    <li> {{ member.education4 }} </li>
    <li> {{ member.education5 }} </li>
    <li> {{ member.education6 }} </li>
    {% endif %}

    </ul>
  </div>
{% endfor %}

## Members
{% assign number_printed = 0 %}
{% for member in site.data.team_members %}

{% assign even_odd = number_printed | modulo: 3 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <b>{{ member.info }}</b>
  <ul style="overflow: hidden">

  {% if member.number_educ == 1 %}
  <li> {{ member.education1 }} </li>
  {% endif %}

  {% if member.number_educ == 2 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  {% endif %}

  {% if member.number_educ == 3 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  {% endif %}

  {% if member.number_educ == 4 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  <li> {{ member.education4 }} </li>
  {% endif %}

  {% if member.number_educ == 5 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  <li> {{ member.education4 }} </li>
  <li> {{ member.education5 }} </li>
  {% endif %}

  </ul>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

## Alumni

{% assign number_printed = 0 %}
{% for member in site.data.alumni_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>
  {{ member.info }} <br>
  <b>after CMCP Lab:</b> {{ member.after_CMCP_lab }} <br>

  <ul style="overflow: hidden">

  </ul>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}
