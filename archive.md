---
layout: default
title: Post Archive
---

<ul class="list-unstyled">
  {% for post in site.posts %}
    <h3 class="text-primary"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
    <div class="border-dark border-top border-bottom mb-3">
        <div class="d-inline">
            <i class="fa fa-calendar-alt"></i>
            <time>{{ post.date | date_to_string }}</time>
        </div>
        <ul class="list-inline float-right">
            {% for tag in post.tags %}
            <li class="list-inline-item">{{ tag }}</li>
            {% endfor %}
        </ul>
    </div>
    <div class="mb-3">
    {{ post.description }}
    </div>
  {% endfor %}
</ul>
