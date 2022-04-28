---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: "Nerd Weekend!"
---

# About

We've done so many of these now, the memories are fading. This is a place to accumulate them.  If you remember anything I've missed, or have a photo to add, there is a link at the bottom of each page to email me (it will reference the current page) and I'll update it.
# Current Proposal

_Doodle has updated and is a lot worse.  This is **technically** not Doodle, but I'll still call it that._

It's time to start talking about the next Nerd Weekend!

Click the doodle.  Click it!

<a href="https://xoyondo.com/dp/FXW7VLzdnc7rIU4" target="_blank">
  <img src="/pics/doodle.png" width="100"/>
</a>

# History

<!--
  Creating markdown table inside Jekyll loop:
  https://stackoverflow.com/a/35643035/5329728

  Embedding list inside table:
  https://stackoverflow.com/a/57904161/5329728

  Set table column width:
  https://stackoverflow.com/a/57420043/5329728
-->

| {::nomarkdown}<div style="width:175px">Date</div>{:/} | {::nomarkdown}<div style="width:175px">Venue</div>{:/}  | Summary |
|---|---|---|
{% for post in site.posts -%}

{% assign post_img_dir = post.path | slice: 7, 7 -%}
{% assign post_img_exists = false -%}
{%- for static_file in site.static_files -%}
{% if static_file.path contains post_img_dir %}
{% assign post_img_exists = true -%}
{% endif %}
{%- endfor -%}

| [{{ post.title }}]({{post.url}}) {% if post_img_exists %}<br>(PICS) {% endif %}| {{post.venue}} | {{post.summary}} |
{% endfor %}

<!-- 
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a><br>
      <em>{{post.venue}}</em><br>
      {{post.summary}}
    </li>
  {% endfor %}
</ul>
-->