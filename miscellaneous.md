---
layout: default
title: "Miscellaneous | Khang Nguyen"
permalink: /miscellaneous/
---

# Miscellaneous

{% assign posts = site.posts | sort: "date" | reverse %}

{% if posts.size > 0 %}
<ul>
{% for post in posts %}
    <li>
        <time datetime="{{ post.date | date_to_xmlschema }}">
            {{ post.date | date: "%Y-%m-%d" }}
        </time>
        —
        <a href="{{ post.url | relative_url }}">
            {{ post.title | escape }}
        </a>

        {% assign description = post.description | default: "" | strip %}
        {% if description != "" %}
        <p class="post-description">{{ description | escape }}</p>
        {% endif %}
    </li>
{% endfor %}
</ul>
{% else %}
<p>No posts yet.</p>
{% endif %}