---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
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

| Date | Venue | Memories |
|---|---|---|
{% for post in site.posts -%}
| {{ post.date_range }} | {{post.venue}} | {% if post.show_link %}[Pics]({{post.url}}) {% endif %}{::nomarkdown}<ul>{% for game in post.games -%} <li>{{game.game}} {% if game.memories %} <ul> {% for memory in game.memories -%}<li>{{memory.memory}}</li>{% endfor %}</ul> {% endif %}</li> {% endfor %} </ul>{:/} |
{% endfor %}