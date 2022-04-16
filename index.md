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
-->

| Date | Venue | Memories
|---|---|---|
{% for date in site.data.dates.dates -%}
| {{ date.date }} | {{date.location}} |
{%- endfor -%}
