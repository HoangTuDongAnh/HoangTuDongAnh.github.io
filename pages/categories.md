---
title: "Chuyên mục"
layout: Post
permalink: /categories
content-type: "static"
description: "Danh sách chuyên mục chính của blog."
---

<p class="page-intro">Chuyên mục dùng cho nhóm nội dung lớn. Mỗi bài viết có thể thuộc một hoặc nhiều chuyên mục.</p>

<div class="tag-cloud">
{% assign categories = site.categories | sort %}
{% for category in categories %}
  <a class="tag-pill" href="#{{ category[0] | slugify }}">{{ category[0] }} <span>{{ category[1].size }}</span></a>
{% endfor %}
</div>

{% for category in categories %}
<section class="archive-section" id="{{ category[0] | slugify }}">
  <h2>{{ category[0] }}</h2>
  <div class="archive-list">
  {% assign category_posts = category[1] | sort: "date" | reverse %}
  {% for post in category_posts %}
    <article class="archive-item">
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%d/%m/%Y" }}</time>
    </article>
  {% endfor %}
  </div>
</section>
{% endfor %}
