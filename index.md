---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---
# Current Proposal

Details of poll dates here

# History

| Date | Venue | Memories |
|---|---|---|
{% for post in site.posts -%}
| {{ post.date }} | {{post.title}} | {{post.venue}} |
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
