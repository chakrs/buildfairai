---
layout: conf_present
permalink: /conf_present/
title: conference presentations
description: I have been submitting my research and presenting at conferences. Following is the list of my conference presentations so far.
nav: false
nav_order: 2
---
<table>
  {% for row in site.data.conf_present %}
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
