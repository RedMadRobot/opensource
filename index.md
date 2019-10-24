---
layout: home
title: Projects
permalink: /
---

{% for group in site.data.repositories %}
## {{ group.name }}

<table>
  {% for repository in group.repositories %}
    <tr>
      <td>
        <a href="https://github.com/redmadrobot/{{ repository.repository }}">
          {{ repository.name }}
        </a>
      </td>
      <td>{% include github_stars repository=repository.repository %}</td>
      <td>{% include github_issues repository=repository.repository %}</td>
      <td>{{ repository.description }}</td>
    </tr>
  {% endfor %}
</table>

{% endfor %}
