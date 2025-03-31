---
title: Běžecký log
layout: base
eleventyNavigation:
  key: Log
---
<div class="table-heading">

__Jaro 2025__ 

_(20.3. - 20.6.2025)_
</div>

<table class="table-overview">
<tr>
    <th>Týden</th>
    <th>Km</th>
    <th>Tempo</th>
    <th>Avg HR</th>
    <th>Kopce</th>
    <th class="hidden-stuff">Čas</th>
  </tr>
  <tr class="unit-cell">
    <td>#</td>
    <td>km</td>
    <td>min/km</td>
    <td>bpm</td>
    <td>m</td>
    <td class="hidden-stuff">hh:mm:ss</td>
  </tr>
  {% for item in weekly %}
  <tr class="data-cell">
    <td>{{ item.Week }}</td>
    <td>{{ item.Distance }}</td>
    <td>{{ item.Pace }}</td>
    <td>{{ item.AvgHR }}</td>
    <td>{{ item.Ascent }}</td>
    <td class="hidden-stuff">{{ item.Duration }}</td>
  </tr>
  {% endfor %}
</table>