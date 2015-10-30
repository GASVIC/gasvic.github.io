---
layout: main
---
# Show history

History is available for the following shows:
{% for pg in site.pages %}
{% if pg.url contains "/shows/" and pg.url != page.url %}
* [{{pg.title}}]({{pg.url}})
{% endif %}
{% endfor %}
