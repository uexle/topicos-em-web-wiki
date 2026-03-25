---
layout: page
title: Início
---

## Artigos da wiki

Novos arquivos `.md` na pasta `_wiki/` passam a aparecer nesta lista automaticamente após o build (no GitHub Pages, após o push).

<ul class="wiki-list">
{% assign pages = site.wiki | sort: 'title' %}
{% for p in pages %}
  <li><a href="{{ p.url | relative_url }}">{{ p.title }}</a></li>
{% endfor %}
</ul>

{% if site.wiki.size == 0 %}
<p><em>Nenhum artigo ainda. Adicione um arquivo em <code>_wiki/</code>.</em></p>
{% endif %}
