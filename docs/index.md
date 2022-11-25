---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

>Over the last few years I have spent a lot of time noting down recipes that repeatedly come back to. Now that my notebook is practically full (this is _1-10-2022_), I have realized that I need to write these recipes down. This is an attempt to document and organize these recipes.
>
>A lot of my cooking is by experimentation, and I have also included at least one (maybe more in the future) real cooking/baking experiment. :)

{% for collection in site.collections %}
<h3>{{ collection.name }}</h3>
<ul>
{% for recipe in site[collection.label] %}
    <li><a href="{{ recipe.url }}">{{ recipe.title }}</a></li>
{% endfor %}
</ul>
{% endfor %}
