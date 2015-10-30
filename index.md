---
layout: main
---
# Gilbert & Sullivan Opera Victoria

This is a simple markdown file, which could be our home page.

Example second paragraph. Lorem ipsum dolor sit amet. Proof of edit.

This site primarily stores show history.

## Upcoming shows

{% for post in site.posts %}
* {{ post.month }} {{ post.year }}: [{{ post.title }}]({{ post.url }})
{% endfor %}

## Archive

### By decade

Not yet implemented.

### By show

* [Pirates of Penzance](shows/pirates.html)
* [Princess Ida](shows/princessida.html)
