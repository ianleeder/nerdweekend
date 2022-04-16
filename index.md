---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---
# Current Proposal

Details of poll dates here

# History

<table>
  {% for post in site.posts %}
    <tr>
      <td>foo</td>
      <td>
        <a href="{{ post.url }}">{{ post.title }}</a>
      </td>
      <td>bar</td>
    </tr>
  {% endfor %}
</table>

<table>
  {% for date in site.data.dates.dates %}
    <tr>
      <td>foo</td>
      <td>
      {{ date.date }}
      </td>
      <td>bar</td>
    </tr>
  {% endfor %}
</table>