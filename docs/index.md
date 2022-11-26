---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---


{% for collection in site.collections %}
<h3>{{ collection.name }}</h3>
<ul>
{% for recipe in site[collection.label] %}
    <li><a href="{{ site.baseurl }}{{ recipe.url }}">{{ recipe.title }}</a></li>
{% endfor %}
</ul>
{% endfor %}
