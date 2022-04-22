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

  Set table column width:
  https://stackoverflow.com/a/57420043/5329728
-->

| {::nomarkdown}<div style="width:175px">Date</div>{:/} | Venue | Summary |
|---|---|---|
{% for post in site.posts -%}
| [{{ post.title }}]({{post.url}}) | {{post.venue}} | {{post.summary}} |
{% endfor %}

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a><br>
      <em>{{post.venue}}</em><br>
      {{post.summary}}
    </li>
  {% endfor %}
</ul>