# Blog Công nghệ của Hoàng

Đây là source blog cá nhân dùng **Jekyll + GitHub Pages + GitHub Actions**, tối ưu cho workflow viết bài bằng **Obsidian** và Markdown.

## 1. Cấu trúc quan trọng

```text
.
├── _config.yml              # cấu hình site, menu, SEO, collection, permalink
├── _posts/                  # bài blog có ngày xuất bản
├── _notes/                  # ghi chú/digital garden từ Obsidian
├── pages/                   # trang tĩnh: home, blog, tags, about...
├── _layouts/Post.html       # layout chính
├── _includes/               # các khối tái sử dụng: sidebar, search, post card...
├── assets/css/style.css     # giao diện
├── assets/js/Search.js      # tìm kiếm client-side bằng Lunr
├── SearchData.json          # dữ liệu search được Jekyll render khi build
└── .github/workflows/       # GitHub Actions deploy lên Pages
```

## 2. Chạy local

Cài Ruby và Bundler, sau đó chạy:

```bash
bundle install
bundle exec jekyll serve
```

Mở trình duyệt tại:

```text
http://localhost:4000
```

Khi đổi `_config.yml`, hãy dừng server và chạy lại `bundle exec jekyll serve`.

## 3. Viết bài blog

Bài blog nằm trong `_posts/` và tên file **bắt buộc** theo dạng:

```text
YYYY-MM-DD-ten-bai-viet.md
```

Ví dụ:

```text
_posts/2026-05-01-cach-dung-jekyll-voi-obsidian.md
```

Front matter mẫu:

```yaml
---
title: "Cách dùng Jekyll với Obsidian"
description: "Quy trình biến ghi chú Markdown trong Obsidian thành blog tĩnh bằng Jekyll."
date: 2026-05-01
author: "Hoàng"
categories:
  - Jekyll
  - Blogging
tags:
  - jekyll
  - obsidian
  - github-pages
feed: show
---
```

## 4. Viết ghi chú từ Obsidian

Ghi chú nằm trong `_notes/`. Mỗi note nên có front matter:

```yaml
---
title: "Tên ghi chú"
date: 2026-05-01
feed: show
---
```

Bạn có thể dùng wiki link giống Obsidian:

```markdown
Đọc thêm [[Thiết kế một prompt tốt]] hoặc [[Jekyll::https://jekyllrb.com]].
```

Alias cũng được hỗ trợ:

```markdown
[[Thiết kế một prompt tốt|bài hướng dẫn prompt]]
```

Embed ảnh kiểu Obsidian:

```markdown
![[assets/img/posts/demo.png]]
```

Nên đặt ảnh trong `assets/img/posts/` để dễ quản lý.

## 5. Deploy lên GitHub Pages

Workflow nằm tại `.github/workflows/jekyll.yml`. Mỗi khi push lên branch `main`, GitHub Actions sẽ:

1. Checkout source.
2. Setup Ruby.
3. Cài gem bằng Bundler cache.
4. Build Jekyll.
5. Upload `_site` làm Pages artifact.
6. Deploy lên GitHub Pages.

Trong GitHub repository, vào **Settings → Pages** và chọn **Build and deployment → Source: GitHub Actions**.

## 6. Tùy chỉnh nhanh

- Đổi tên blog, mô tả, URL: sửa `_config.yml`.
- Đổi menu: sửa `menu:` trong `_config.yml`.
- Đổi màu/font/layout: sửa `assets/css/style.css`.
- Đổi trang giới thiệu: sửa `pages/about.md`.
- Đổi trang chủ: sửa `pages/index.md`.

## 7. Checklist trước khi publish

- File bài viết trong `_posts/` có dạng `YYYY-MM-DD-slug.md`.
- Mỗi bài có `title`, `description`, `date`, `categories`, `tags`.
- Ảnh không để rải rác ở root, ưu tiên `assets/img/posts/`.
- Không commit `_site/`, `.jekyll-cache/`, `.DS_Store`, workspace riêng của Obsidian.
- Build local không báo lỗi trước khi push.
