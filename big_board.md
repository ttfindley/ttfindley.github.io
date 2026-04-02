---
layout: default
title: 2025 Draft Big Board
---

<div class="hero" style="padding:48px 40px 40px">
  <div class="hero-label">2025 NFL Draft</div>
  <h1 class="hero-title" style="font-size:36px">Big Board</h1>
  <p class="hero-sub">Click any prospect to view their full scouting profile, combine data, and grade.</p>
</div>

<div class="section">
<table id="big-board">
  <tr>
    <th>Rank</th>
    <th>Name</th>
    <th>Position</th>
    <th>School</th>
  </tr>
  {% for player in site.data.big_board %}
  <tr>
    <td>{{ player.rank }}</td>
    <td>
      {% if player.profile and player.profile != "" %}
        <a href="{{ player.profile }}">{{ player.name }}</a>
      {% else %}
        {{ player.name }}
      {% endif %}
    </td>
    <td>{{ player.position }}</td>
    <td>{{ player.school }}</td>
  </tr>
  {% endfor %}
</table>
</div>
