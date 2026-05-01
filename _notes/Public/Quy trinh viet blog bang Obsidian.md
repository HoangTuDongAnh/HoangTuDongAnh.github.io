---
title: "Quy trình viết blog bằng Obsidian"
date: 2026-05-01
feed: show
---

Ghi chú này mô tả workflow mình dùng để biến ý tưởng trong Obsidian thành bài blog public bằng Jekyll.

## 1. Ghi nhanh trong `_notes`

Khi ý tưởng còn thô, hãy viết trong `_notes`. Mục tiêu là lưu lại khái niệm, link tham khảo, checklist hoặc code snippet ngắn.

## 2. Gom ý thành outline

Khi một note đủ rõ, tạo outline theo cấu trúc:

- Vấn đề là gì?
- Ai cần đọc?
- Sau bài này người đọc làm được gì?
- Các bước thực hiện ra sao?
- Có lỗi thường gặp nào không?

## 3. Chuyển thành bài trong `_posts`

Tạo file theo dạng:

```text
_posts/YYYY-MM-DD-ten-bai-viet.md
```

Thêm front matter có `title`, `description`, `date`, `categories`, `tags`.

## 4. Kiểm tra local

Chạy:

```bash
bundle exec jekyll serve
```

Sau đó đọc lại trang chủ, trang blog, tag và bài viết mới.

## 5. Publish

Commit và push lên branch `main`. GitHub Actions sẽ build và deploy site lên GitHub Pages.
