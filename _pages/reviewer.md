---
layout: reviewer
permalink: /reviewer/
title: reviewer
description: Professional conference for which I have reviewed submissions
nav: false
nav_order: 1
---
<table>
  {% for row in site.data.reviewer %}
    {% if forloop.first %}
    <tr>
      {% for pair in row %}
        <th>{{ pair[0] }}</th>
      {% endfor %}
    </tr>
    {% endif %}

    {% tablerow pair in row %}
      {{ pair[1] }}
    {% endtablerow %}
  {% endfor %}
</table>
