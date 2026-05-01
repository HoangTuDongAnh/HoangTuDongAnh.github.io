---
title: "Thiết kế một prompt tốt"
description: "Khung tư duy thực tế để viết prompt rõ ràng, có ngữ cảnh và dễ cải tiến khi làm việc với Gen AI."
date: 2026-04-15
author: "Hoàng"
categories:
  - AI
  - Prompt Engineering
tags:
  - prompt
  - gen-ai
  - writing
feed: show
---

Thiết kế prompt là một kỹ năng quan trọng khi làm việc với các công cụ Gen AI. Một prompt tốt giúp AI hiểu rõ bạn muốn gì, cần làm theo hướng nào và nên trả về kết quả ra sao.  
  
Tuy nhiên, prompt tốt không nhất thiết phải dài. Điều quan trọng hơn là prompt cần **rõ ràng, có cấu trúc và có khả năng được cải tiến qua từng lần thử**.  
  
# 1. Vì sao cần thiết kế prompt?  
  
Khi làm việc với Gen AI, chất lượng đầu ra phụ thuộc rất nhiều vào chất lượng đầu vào.  
  
- Output là kết quả bạn muốn nhận được  
- Input là prompt bạn cung cấp cho AI  
- Prompt càng rõ, AI càng dễ tạo ra kết quả đúng ý  
- Prompt càng mơ hồ, output càng dễ chung chung hoặc lệch hướng  
  
Một cách đơn giản để bắt đầu là sử dụng khung 5 bước: **Task, Context, References, Evaluate, Iterate**.  

---
## 1.1. Task (Nhiệm vụ)  
  
**Task** là phần mô tả việc bạn muốn AI thực hiện.  
  
Đây là nền tảng của prompt. Nếu task không rõ, các phần còn lại cũng khó phát huy hiệu quả.  
  
- Mô tả hành động cụ thể:  
- Viết  
- Tóm tắt  
- Phân tích  
- Lên ý tưởng  
- Tạo bảng  
- Viết checklist  
- Tránh yêu cầu quá chung chung  
- Nói rõ kết quả bạn kỳ vọng  
  
### Persona (Vai trò)  
  
Khi cần, hãy yêu cầu AI đóng một vai trò cụ thể.  
  
Ví dụ:  
  
- Chuyên gia marketing  
- Lập trình viên senior  
- Blogger công nghệ  
- Giáo viên dành cho người mới bắt đầu  
- Nhà phân tích ngành  
  
Persona giúp AI chọn góc nhìn phù hợp và loại bỏ những thông tin không cần thiết.  
  
### Format (Định dạng)  
  
Format là cách bạn muốn output được trình bày.  
  
Ví dụ:  
  
- Bullet points  
- Bảng so sánh  
- Checklist  
- Đoạn văn ngắn  
- Outline bài blog  
- Email mẫu  
  
```text  
Bạn là một blogger công nghệ. Hãy viết một checklist dạng bullet points về cách tạo prompt tốt cho người mới bắt đầu.  
```  

---
## 1.2. Context (Ngữ cảnh)  
  
**Context** là phần thông tin nền giúp AI hiểu rõ tình huống.  
  
Prompt có context tốt sẽ giúp AI trả lời sát nhu cầu hơn, thay vì đưa ra câu trả lời chung chung.  
  
Bạn có thể bổ sung:  
  
- Mục tiêu của nội dung  
- Đối tượng người đọc  
- Lý do bạn cần output này  
- Phong cách mong muốn  
- Những gì bạn đã thử trước đó  
- Giới hạn hoặc yêu cầu đặc biệt  
  
```text  
Nội dung này sẽ được dùng trong một bài blog tiếng Việt dành cho người mới tìm hiểu về Gen AI. Hãy viết ngắn gọn, dễ hiểu và có ví dụ thực tế.  
```  
  
> Context thường là phần có thể dài nhất trong prompt, vì nó giúp AI hiểu rõ “bối cảnh sử dụng” của output.  

---
## 1.3. References (Tham chiếu)  
  
**References** là các ví dụ, tài liệu mẫu hoặc phong cách bạn muốn AI tham khảo.  
  
Đây là cách rất hiệu quả để định hướng output.  
  
Bạn có thể cung cấp:  
  
- Một đoạn văn mẫu  
- Một cấu trúc bài viết  
- Một ví dụ output mong muốn  
- Một tài liệu tham khảo  
- Một phong cách viết cụ thể  
  
### Cách trình bày references rõ ràng  
  
Hãy đánh dấu phần tham chiếu để AI hiểu đâu là tài liệu mẫu.  
  
```text  
Dựa theo ví dụ sau:  
  
### Sample  
"Nội dung mẫu..."  
```  
  
Hoặc dùng XML-style tags khi prompt phức tạp hơn:  
  
```xml  
<example>  
Nội dung mẫu đặt ở đây  
</example>  
```  
  
> Không cần đưa quá nhiều ví dụ. Thông thường, 2–5 references chất lượng là đủ.  

---
## 1.4. Evaluate (Đánh giá)  
  
Không nên sử dụng output đầu tiên một cách máy móc.  
  
Sau khi AI trả lời, hãy tự đánh giá:  
  
- Output có đúng yêu cầu ban đầu không?  
- Có rõ ràng và logic không?  
- Có phù hợp với đối tượng người đọc không?  
- Có thiếu thông tin quan trọng không?  
- Có thông tin nào cần kiểm chứng lại không?  
- Giọng văn đã đúng với mục tiêu chưa?  
  
AI có thể tạo ra những kết quả khác nhau ngay cả khi bạn dùng cùng một prompt. Vì vậy, bước đánh giá giúp bạn quyết định nên dùng, chỉnh sửa hay tiếp tục cải tiến prompt.  

---
## 1.5. Iterate (Lặp lại)  
  
**Iterate** nghĩa là tiếp tục điều chỉnh prompt dựa trên output nhận được.  
  
Đây cũng là tinh thần của nguyên tắc **ABI — Always Be Iterating**.  
  
Thay vì xoá toàn bộ prompt và bắt đầu lại từ đầu, hãy xem output hiện tại như một bản nháp để cải thiện.  
  
- Xác định phần chưa đúng  
- Bổ sung thông tin còn thiếu  
- Điều chỉnh vai trò hoặc định dạng  
- Thêm ví dụ tham chiếu  
- Thêm ràng buộc  
- Thử cách diễn đạt khác  
  
> Prompt tốt thường không xuất hiện ngay từ lần đầu, mà được tinh chỉnh qua nhiều vòng lặp.  

### ABI: Always Be Iterating  
  
ABI là cách tiếp cận giúp bạn cải thiện prompt liên tục.  
  
Quy trình đơn giản:  
  
- Viết prompt đầu tiên  
- Xem output  
- Đánh giá điểm chưa đạt  
- Điều chỉnh prompt  
- Tiếp tục thử lại trong cùng một cuộc trò chuyện  
  
Khi lặp lại prompt trong cùng một chat, AI có thể dựa vào những thông tin bạn đã cung cấp trước đó để hiểu ngữ cảnh tốt hơn.  

---
# 2. Bốn cách cải tiến prompt hiệu quả  
  
Ngay cả khi đã có framework, đôi khi output vẫn chưa đúng ý. Khi đó, bạn có thể dùng bốn phương pháp dưới đây để cải thiện prompt.  
  
## 2.1. Quay lại khung prompt ban đầu  
  
Nếu output quá chung chung, hãy kiểm tra lại prompt có đủ các thành phần quan trọng chưa:  
  
- Task đã rõ chưa?  
- Có persona chưa?  
- Có format chưa?  
- Context đã đủ cụ thể chưa?  
- Có references phù hợp chưa?  
  
**Prompt chưa tối ưu**
```text  
Identify the latest developments in the restaurant industry.  
```  
  
Prompt này chỉ có task, nên AI có thể trả lời rất rộng và thiếu trọng tâm.  
  
**Prompt được cải thiện**
```text  
Create a bulleted list including the latest developments in the restaurant industry specific to urban areas that could impact the public reception of a dining experience using only ingredients native to the region.  
```  
  
Prompt mới tốt hơn vì đã bổ sung:  
  
- Định dạng output  
- Phạm vi cụ thể  
- Bối cảnh ngành  
- Mục tiêu phân tích rõ hơn  
  
## 2.2. Chia prompt dài thành nhiều bước nhỏ  
  
Một prompt dài với quá nhiều yêu cầu có thể khiến AI xử lý thiếu chính xác.  
  
Thay vì nhồi nhiều nhiệm vụ vào một prompt, hãy tách thành từng bước.  
  
**Prompt quá dài**
  
```text  
Summarize the key data points and information in this report. Then create visual graphs from the data and shorten the key information into bullets.  
```  
  
**Cách chia nhỏ tốt hơn**
  
```text  
First, summarize the key data points and information in this report.  
```  
  
Sau đó tiếp tục:  
  
```text  
Create visual graphs from the data you summarized.  
```  
  
Cuối cùng:  
  
```text  
Shorten the key information you summarized into bullets.  
```  
  
Cách này giúp AI tập trung vào từng nhiệm vụ nhỏ, từ đó output thường rõ và chính xác hơn.  
  
## 2.3. Thử cách diễn đạt khác hoặc dùng nhiệm vụ tương tự  
  
Nếu prompt hiện tại chưa cho kết quả tốt, hãy thử diễn đạt lại theo hướng khác.  
  
Bạn cũng có thể dùng **analogous task** — một nhiệm vụ tương tự với nhiệm vụ chính, nhưng được đặt trong một góc tiếp cận mới.  
  
**Ví dụ**
  
- Thay vì viết:  
  
```text  
Write a marketing plan for this product.  
```  
  
- Bạn có thể thử:  
  
```text  
Write a story about how this product fits into the daily life of our target customer.  
```  
  
Cả hai đều hướng đến mục tiêu marketing, nhưng cách thứ hai buộc AI suy nghĩ theo hướng kể chuyện và trải nghiệm người dùng.  
  
**Ví dụ trong ngành nhà hàng**
  
- Thay vì hỏi:  

```text  
Identify the latest developments in the restaurant industry.  
```  
  
- Bạn có thể viết:  
  
```text  
I’m starting a restaurant that will only include produce from within 50 miles. You’re a diner that lives in a major city and keeps up with the latest restaurant trends. Write a list of questions that I should consider before opening up the restaurant.  
```  
  
Cách đặt vấn đề này giúp AI nhìn bài toán từ góc nhìn của khách hàng, thay vì chỉ liệt kê xu hướng chung.  
  
## 2.4. Thêm ràng buộc để định hướng output  
  
Ràng buộc giúp AI thu hẹp phạm vi trả lời và tạo ra kết quả cụ thể hơn.  
  
Bạn có thể thêm ràng buộc về:  
  
- Độ dài  
- Định dạng  
- Đối tượng người đọc  
- Khu vực địa lý  
- Thời gian  
- Phong cách  
- Loại thông tin được phép hoặc không được phép dùng  
  
**Ví dụ đơn giản**
  
- Thay vì yêu cầu:  
  
```text  
Give me some food recipes.  
```  
  
- Hãy cụ thể hơn:  
  
```text  
Give me five dinner recipes that use seasonal ingredients and take less than 30 minutes to prepare.  
```  
  
**Ví dụ nâng cao**
  
```text  
Create a bulleted list including the latest developments in the restaurant industry specific to urban areas that could impact the public reception of a dining experience using only ingredients native to the region. This list should only include trends from cities with a population of more than 500,000 people, and should only include trends relevant to vegetarian and vegan restaurants.  
```  
  
Ràng buộc không làm prompt kém sáng tạo. Ngược lại, nó giúp AI tạo ra kết quả đúng trọng tâm và có tính ứng dụng cao hơn.  

---
# 3. Công thức gợi ý để viết prompt tốt
  
Bạn có thể dùng cấu trúc sau khi viết prompt:  
  
```text  
Bạn là [persona].  
Hãy thực hiện [task].  
Bối cảnh là [context].  
Tham khảo [references].  
Trình bày dưới dạng [format].  
Lưu ý các ràng buộc sau: [constraints].  
```  
  
### Ví dụ hoàn chỉnh  
  
```text  
Bạn là một blogger công nghệ chuyên viết cho người mới bắt đầu.  
  
Hãy viết một bài blog ngắn giải thích cách tạo prompt tốt khi sử dụng Gen AI.  
  
Bối cảnh: Bài viết dành cho độc giả tiếng Việt chưa có nhiều kinh nghiệm với AI. Nội dung cần dễ hiểu, thực tế và có ví dụ minh họa.  
  
Trình bày dưới dạng Markdown, có heading rõ ràng, bullet points ngắn và phần tổng kết cuối bài.  
  
Không dùng thuật ngữ quá học thuật. Giữ giọng văn thân thiện và dễ đọc.  
```  

---
# 4. Tổng kết  
  
Thiết kế một prompt tốt không chỉ là viết một câu yêu cầu cho AI. Đó là quá trình xác định đúng nhiệm vụ, cung cấp đủ ngữ cảnh, đưa ví dụ tham khảo, đánh giá output và liên tục cải tiến.  
  
Một prompt tốt thường có:  
  
- **Task rõ ràng**  
- **Context đầy đủ**  
- **References phù hợp**  
- **Output format cụ thể**  
- **Ràng buộc hợp lý**  
- **Quá trình iterate liên tục**  
  
---  
  
*Prompt tốt không phải là prompt hoàn hảo ngay từ đầu. Prompt tốt là prompt được thiết kế có chủ đích và được cải tiến sau mỗi lần sử dụng.*