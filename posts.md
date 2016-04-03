---
layout: page
title: posts
permalink: /posts/
---

<div class="post-list">
    {% for post in site.posts %}
      <div class="post">
        <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
        <p class="post-meta">
          {{ post.date | date_to_rfc822 }}
          </p><p class="post-meta">
          <span>
            <span class="icon-price-tags"></span>
            {% for tag in post.tags %}
            {{ tag | xml_escape }}
            {% endfor %}
          </span>
          <span>
            {% for cat in post.categories %}
            {{ cat | xml_escape }}
            {% endfor %}
          </span>
        </p>
      </div>
    {% endfor %}
</div>

