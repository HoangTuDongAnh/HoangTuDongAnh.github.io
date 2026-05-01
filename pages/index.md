---
layout: Post
permalink: /
title: "Blog Công nghệ của Hoàng"
description: "Blog cá nhân về AI, prompt engineering, phát triển phần mềm và ghi chú học tập bằng Obsidian."
---

<section class="hero-section">
  <p class="eyebrow">IT Blog · Jekyll · Obsidian</p>
  <h1>Viết, ghi chú và chia sẻ kiến thức công nghệ theo cách bền vững.</h1>
  <p class="hero-lead">Đây là không gian để mình biến ghi chú Obsidian thành bài blog có cấu trúc: có bài viết mới, tag/chuyên mục, tìm kiếm, RSS, sitemap và quy trình deploy tự động bằng GitHub Actions.</p>
  <div class="hero-actions">
    <a class="btn" href="{{ '/blog' | relative_url }}">Đọc blog</a>
    <a class="btn ghost" href="{{ '/notes' | relative_url }}">Xem ghi chú</a>
  </div>
</section>

<section class="feature-grid" aria-label="Chủ đề chính">
  <article class="feature-card">
    <span>01</span>
    <h2>AI & Prompt</h2>
    <p>Cách thiết kế prompt, làm việc với Gen AI và kiểm chứng kết quả theo hướng thực tế.</p>
  </article>
  <article class="feature-card">
    <span>02</span>
    <h2>Jekyll & GitHub Pages</h2>
    <p>Ghi lại quá trình xây dựng blog tĩnh, tối ưu giao diện và triển khai tự động.</p>
  </article>
  <article class="feature-card">
    <span>03</span>
    <h2>Obsidian Workflow</h2>
    <p>Viết bằng Markdown, liên kết kiểu wiki link và biến ghi chú thành nội dung public.</p>
  </article>
</section>

<section class="home-section">
  <div class="section-heading">
    <p class="eyebrow">Mới nhất</p>
    <h2>Bài viết gần đây</h2>
  </div>
  <div class="post-list home-posts">
    {% assign featured_posts = site.posts | where_exp: "post", "post.feed != 'hide'" | sort: "date" | reverse %}
    {% for post in featured_posts limit: 3 %}
      {% include PostCard.html item=post %}
    {% endfor %}
  </div>
</section>

<section class="home-section split-section">
  <div>
    <p class="eyebrow">Tìm kiếm</p>
    <h2>Tìm nhanh trong blog</h2>
    <p>Gõ từ khóa để tìm bài viết, ghi chú hoặc trang hướng dẫn. Công cụ tìm kiếm chạy ngay trên trình duyệt bằng Lunr.js.</p>
  </div>
  {% include Search.html %}
</section>
