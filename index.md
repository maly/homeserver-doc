---
layout: single
title: Jak jsem dělal domácí server
excerpt: Série článků (kapitol) o tom, jak jsem stavěl a provozuju domácí server. Subjektivně, ale s kompletními příkazy.
---

## Kapitoly
{% assign items = site.homeserver | sort: "order" %}
{% for p in items %}
- [{{ p.title }}]({{ p.url }})
{% endfor %}
