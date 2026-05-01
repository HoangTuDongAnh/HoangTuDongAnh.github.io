# Hướng dẫn dùng Obsidian để viết blog Jekyll

## Workflow đề xuất

1. Mở thư mục repo này bằng Obsidian.
2. Viết ý tưởng nhanh trong `_notes/`.
3. Khi một note đủ tốt, chuyển nó thành bài blog trong `_posts/`.
4. Thêm front matter đầy đủ: title, description, date, categories, tags.
5. Chạy local bằng `bundle exec jekyll serve` để kiểm tra.
6. Commit và push lên GitHub.

## Khi nào dùng `_notes`?

Dùng `_notes` cho kiến thức dạng evergreen, chưa cần cấu trúc như bài blog hoàn chỉnh. Ví dụ: khái niệm, checklist, snippet, tài liệu học tập.

## Khi nào dùng `_posts`?

Dùng `_posts` cho nội dung có ngày xuất bản, có mở bài/thân bài/kết luận rõ ràng. Ví dụ: tutorial, review công cụ, bài phân tích, case study.

## Quy tắc ảnh

Đặt ảnh vào:

```text
assets/img/posts/
```

Trong bài viết có thể dùng Markdown chuẩn:

```markdown
![Mô tả ảnh]({{ '/assets/img/posts/ten-anh.png' | relative_url }})
```

Hoặc Obsidian embed:

```markdown
![[assets/img/posts/ten-anh.png]]
```

## Quy tắc đặt tên

Tên file nên không dấu để URL sạch hơn:

```text
2026-05-01-huong-dan-jekyll-github-pages.md
```

Tiêu đề trong front matter vẫn viết tiếng Việt có dấu bình thường.
