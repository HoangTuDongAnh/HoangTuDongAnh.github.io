---
title: "Tags"
layout: Post
permalink: /tags
content-type: "static"
description: "Danh sách tag dùng trong blog."
---

<p class="page-intro">Tag giúp người đọc đi theo một chủ đề nhỏ xuyên suốt nhiều bài viết.</p>

<div class="tag-cloud">
{% assign tags = site.tags | sort %}
{% for tag in tags %}
  <a class="tag-pill" href="#{{ tag[0] | slugify }}">#{{ tag[0] }} <span>{{ tag[1].size }}</span></a>
{% endfor %}
</div>

{% for tag in tags %}
<section class="archive-section" id="{{ tag[0] | slugify }}">
  <h2>#{{ tag[0] }}</h2>
  <div class="archive-list">
  {% assign tagged_posts = tag[1] | sort: "date" | reverse %}
  {% for post in tagged_posts %}
    <article class="archive-item">
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%d/%m/%Y" }}</time>
    </article>
  {% endfor %}
  </div>
</section>
{% endfor %}
