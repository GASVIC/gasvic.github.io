---
layout: main
---
# Show history

History is available for the following shows:
{% for pg in site.pages %}
{% if pg.url contains "/shows/" %}
* [{{ pg.date | date: "%b %Y" }} {{pg.title}}]({{pg.url}})
{% endif %}
{% endfor %}
