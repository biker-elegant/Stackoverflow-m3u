---
layout: home
---

- [play.m3u](https://biker-elegant.github.io/Stackoverflow-m3u/static_files/play.m3u)

{% for file in site.static_files %}
{% if file.extname == ".mp3" %}
{% assign filename = file.basename | replace: "-", " " | replace: "_", " " %}
{% assign filepath = file.path | relative_url %}

<a href="{{ filepath }}" title="{{ filename }}">{{ filename }}</a>
<hr>

{% endif %}
{% endfor %}