---
title: Khai phá sức mạnh của Multimodal Prompting
feed: show
date: 2026-04-15
---
Trong thế giới Gen AI, prompt không còn chỉ là văn bản. Bạn có thể kết hợp **text, hình ảnh, âm thanh, video hoặc code** để tạo ra những kết quả mạnh mẽ hơn. Đây chính là **multimodal prompting** — một cách tiếp cận giúp AI hiểu vấn đề toàn diện hơn và tạo ra output chính xác, sáng tạo hơn.  
  
## Multimodal Prompting là gì?  
  
Multimodal prompting là việc sử dụng **nhiều loại dữ liệu (modalities)** trong cùng một prompt:  
  
- Text → mô tả nhiệm vụ  
- Image → cung cấp ngữ cảnh trực quan  
- Audio → nội dung cần phân tích  
- Video → hành vi, sự kiện  
- Code → logic hoặc cấu trúc  
  
👉 Thay vì chỉ “nói”, bạn đang **“cho AI thấy” và “cho AI nghe”**.  
  
## Vì sao multimodal lại quan trọng?  
  
Trong thực tế, con người không chỉ xử lý thông tin qua chữ.  
  
- Bạn nhìn biểu đồ → hiểu nhanh hơn đọc số liệu  
- Bạn nghe giọng nói → hiểu cảm xúc  
- Bạn xem hình ảnh → nắm bắt ngữ cảnh  
  
Multimodal prompting giúp AI **tiếp cận thông tin giống cách con người làm** → kết quả tự nhiên và hữu ích hơn.  
  
## Text vs Image Prompting: khác gì?  
  
### Prompt text  
  
```text  
Generate headlines for a rock concert poster in New Orleans.  
```  
  
- Tập trung vào nội dung chữ  
- Cần rõ task + context  
- Output là văn bản  
  
### Prompt hình ảnh  
  
```text  
Generate an image of an electric guitar in a photographic style. The guitar should be glittery, placed in the foreground and appear to float in the sky.  
```  
  
- Cần mô tả chi tiết hơn:  
- Màu sắc  
- Vị trí  
- Phong cách  
- Cảm xúc  
  
👉 Image prompting yêu cầu **mô tả “giàu hình ảnh” hơn text prompting**.  
  
## Iteration trong multimodal  
  
Dù là text hay image, bạn vẫn cần iterate.  
  
Ví dụ:  
  
- Output chưa đủ “ngầu” → thêm hiệu ứng  
- Thêm chi tiết: ánh sáng, thời tiết, góc nhìn  
  
```text  
Make the sky stormy with lightning hitting the guitar.  
```  
  
👉 Mỗi lần iterate = thêm chi tiết → output gần hơn với ý tưởng ban đầu.  
  
## Ứng dụng thực tế của Multimodal Prompting  
  
### 1. Tạo nội dung từ hình ảnh  
  
- Upload ảnh sản phẩm → viết caption  
- Upload thiết kế → tạo nội dung marketing  
  
```text  
Write a social media caption for this nail art image. Keep it fun and short.  
```  
  
### 2. Phân tích dữ liệu từ hình ảnh  
  
- Chụp biểu đồ → yêu cầu giải thích  
- Chụp tài liệu → trích xuất thông tin  
  
### 3. Làm việc với tài liệu thực tế  
  
- Ảnh lịch sự kiện → trích xuất timeline  
- Sơ đồ văn phòng → liệt kê phòng ban  
  
```text  
Extract keynote times and panel sessions into a table.  
```  
  
### 4. Xử lý audio  
  
- Ghi âm → chuyển thành text  
- Dịch ngôn ngữ  
  
## Kết hợp framework khi dùng multimodal  
  
Dù dùng modality nào, vẫn nên giữ cấu trúc:  
  
- Task: bạn muốn gì?  
- Context: dùng để làm gì?  
- Format: output ra sao?  
- References: có mẫu không?  
  
👉 Multimodal không thay thế framework — nó **mở rộng framework**.  
  
## Multimodal = cộng tác với AI  
  
Một điểm quan trọng:  
  
- Không phải “ra lệnh → nhận kết quả”  
- Mà là **đối thoại liên tục**  
  
Bạn:  
  
- Đưa input  
- Nhận output  
- Điều chỉnh  
- Thử lại  
  
Giống như làm việc với designer:  
  
- “Logo này ổn, nhưng màu chưa đúng”  
- “Style này ok, nhưng đơn giản hơn chút”  
  
👉 Multimodal prompting biến AI thành **một cộng sự sáng tạo**.  
  
## Khi nào nên dùng multimodal?  
  
Sử dụng khi:  
  
- Văn bản không đủ mô tả  
- Cần hiểu ngữ cảnh trực quan  
- Làm việc với dữ liệu thực tế (ảnh, tài liệu, audio)  
- Muốn tăng tốc công việc  
  
## Tổng kết  
  
Multimodal prompting mở ra một cách làm việc mới với AI:  
  
- Kết hợp nhiều loại dữ liệu  
- Hiểu vấn đề sâu hơn  
- Tạo output chính xác và sáng tạo hơn  
  
Một prompt tốt trong multimodal vẫn cần:  
  
- Task rõ ràng  
- Context đầy đủ  
- Mô tả chi tiết (đặc biệt với hình ảnh)  
- Iterate liên tục  
  
---  
  
*Bạn không chỉ đang “viết prompt” — bạn đang “giao tiếp đa giác quan” với AI.*