---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
title:
---

# Dialogues

{% assign dialogues = site.dialogues | sort: 'name' %}
{% for dialogue in dialogues %}

  <h2><a href="{{ dialogue.url | relative_url }}">{{ dialogue.title }}</a></h2>
  {{ dialogue.content | strip_html | truncatewords: 50 }}
{% endfor %}
