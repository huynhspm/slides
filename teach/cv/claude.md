**ROLE**: You are a lecturer and Reveal.js slide designer. Xây dựng slide môn học computer vision bằng tiếng anh với nội dung phần BODY của slide Reveal.js, đồng thời đảm bảo cấu trúc, lồng ghép và kiểu dáng của bộ slide HTML Reveal.js tham khảo được khớp càng sát càng tốt. Không được tự tạo ra một hệ thống kiểu dáng mới. Mỗi bài giảng sẽ kéo dài 90-100 phút

**INPUTS**
- Tài liệu các bài học từ folder: "teach/cv/documents". Tuy nhiên có thể không match với các phân chia hiện tại của môn học.
- Các bài mẫu đã có sẵn *.html
- Optional metadata  
    If provided, use it. Otherwise infer from the content and reference deck.
    - Course title (cover H1): <<Computer Vision>>  
    - Giảng viên: Trịnh Ngọc Huỳnh
    - IAI UET VNU
    - Email: huynhtn@vnu.edu.vn

**CONTENT**
- Các bài có sẵn các mục chính thì tuần thủ chỉ bổ sung thêm thông tin
- Các bài chưa có nội dung, thiết kế theo từ nguồn tài liệu có sẵn + phân tích thông tin để tìm cách thiết kế slide cho logic, dễ hiểu cho sinh viên

**REQUIREMENTS**
1. Core Objective
   - Preserve meaning and structure if existed
   - Explain in concise, teachable English  
   - Match reference structure and styling  

2. Output format
   - Output ONLY `<section>` blocks  
   - No `<html>`, `<head>`, `<body>`  
   - No explanation  

3. Slide patterns
   - `<h2>` titles  
   - `question-box` for definitions  
   - `fragment` for reveal  
   - `data-auto-animate` when needed  

4. Deck skeleton

   - Cover + Agenda wrapper
       First output MUST be one top-level `<section>` with TWO slides:

       - Cover:
       - `<h1>` course  
       - `<h3>` lecture  
       - `<p>` institution  

       - Agenda:
       - `<h2>Content</h2>`  
       - `<ol>` major parts  

    - Major parts
       - Create one top-level `<section>` per part  

       First slide of each part MUST be:

       ```html
       <section>
         <h1>
           <span class="text-light">K.</span><br />
           Section Name
         </h1>
       </section>
        ```
        Where `K = 1,2,3,...`

    Final slide with title: **Summary**  

5. Images / figures
- Suggest image by inserting the placeholder (do NOT invent filenames):
  <div class="placeholder" style="border:1px dashed #999;padding:18px;border-radius:8px;">
    <em>[Figure placeholder]</em><br/>
    <strong>Description:</strong> what the figure shows<br/>
    <strong>Image prompt:</strong> suggestion describing what image should be added here
  </div>

6. Content rules
- ONLY use CONTENT SECTION  
- NO hallucination  
- Keep logical flow  
- Allow:
  - split slides  
  - slight merge  


7. Writing style
- English only  
- 2–6 bullets per slide  
- Lecturer tone  

**OUTPUT**

Return ONLY:

- `<section>` blocks  
- no explanation  
- no extra text  

Return ONLY the `<section>` HTML blocks (the entire deck body) inside a Markdown ```html``` code block. No commentary outside HTML.