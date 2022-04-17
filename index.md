---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---
# Current Proposal

Details of poll dates here

# History

<!--
  Embedding list inside table:
  https://stackoverflow.com/a/57904161/5329728
-->

| Date | Venue | Memories |
|---|---|---|
{% for post in site.posts -%}

| {{ post.date_range }} | {{post.venue}} | {::nomarkdown}<ul>{% for game in post.games -%} <li>{{game.game}} {% if game.memories %} <ul> {% for memory in game.memories -%}<li>{{memory.memory}}</li>{% endfor %}</ul> {% endif %}</li> {% endfor %} </ul>{:/} |
{% endfor %}

<ul>
  {% for post in site.posts %}
    <li>
      <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
      {{ post.excerpt }}
    </li>
  {% endfor %}
</ul>

<!-- 
  Creating markdown table inside Jekyll loop:
  https://stackoverflow.com/a/35643035/5329728
-->

| Date | Venue | Memories |
|---|---|---|
{% for date in site.data.dates.dates -%}
| {{ date.date }} | {{date.location}} |
{%- endfor -%}
