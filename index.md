---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: "Nerd Weekend!"
---
# Current Proposal

Details of poll dates here

# History

<!--
  Creating markdown table inside Jekyll loop:
  https://stackoverflow.com/a/35643035/5329728

  Embedding list inside table:
  https://stackoverflow.com/a/57904161/5329728
-->

| Date | Venue | Summary |
|---|---|---|
{% for post in site.posts -%}
| [{{ post.date_range }}]({{post.url}}) | {{post.venue}} | {{post.summary}} |
{% endfor %}