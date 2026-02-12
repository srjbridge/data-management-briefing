---
layout: default
permalink: /
---

# Data Management Briefing

Weekly briefing on data management best practices, open data, and emerging trends in Canada and internationally.

## Latest Briefing

{% for post in site.posts limit:1 %}

**Published:** {{ post.date | date: "%B %d, %Y" }}

{{ post.content }}

{% endfor %}

---

[View Archive →](/archive/) | [About](/about/) | [Subscribe](/subscribe/)
