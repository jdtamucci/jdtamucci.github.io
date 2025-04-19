---
layout: page
title: "Publications"
permalink: /publications/
---

## Peer-Reviewed Research

{% assign sorted = site.publications | sort: 'date' | reverse %}
{% for post in sorted %}
  {% if forloop.index <= 4 %}
  <div>
    <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
    <p><strong>{{ post.authors }}</strong><br>
    <em>{{ post.journal }}</em><br>
    {% if post.doi %}<a href="{{ post.doi }}">View publication</a>{% endif %}
    </p>
  </div>
  {% endif %}
{% endfor %}

## Policy & Public-Facing Publications

{% for post in sorted %}
  {% if forloop.index > 4 %}
  <div>
    <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
    <p><strong>{{ post.authors }}</strong><br>
    <em>{{ post.journal }}</em><br>
    {% if post.doi %}<a href="{{ post.doi }}">View article</a>{% endif %}
    </p>
  </div>
  {% endif %}
{% endfor %}
