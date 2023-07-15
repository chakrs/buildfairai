---
layout: half-marathon
permalink: /half_marathon/
title: half marathons
description: I enjoy training for and running half marathons; Here are some recent half marathon runs that I did... although not great time performance, I am glad that I did it.
nav: false
nav_order: 1
---
<table>
  {% for row in site.data.half_marathons %}
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
