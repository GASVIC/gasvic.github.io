---
layout: main
---
# Gilbert & Sullivan Opera Victoria

This is a simple markdown file, which could be our home page.

Example second paragraph. Lorem ipsum dolor sit amet. Proof of edit.

This site primarily stores show history.

## Upcoming shows

{% for post in site.posts %}
{% if post.date >= site.time %}
* {{ post.date | date: "%b %Y" }}: [{{ post.title }}]({{ post.url }})
{% endif %}
{% endfor %}

## Archive

By decade - not yet implemented.

[By show](shows/)
