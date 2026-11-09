# Báo cáo cá nhân — MSSV_HoTen

> Đổi tên file theo quy tắc `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md` (MSSV trước, dấu `_`, họ tên viết liền không dấu). Sửa cả dòng tiêu đề phía trên cho khớp.
> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: copy template này thành file mới, điền, rồi commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên: Nguyễn Minh Nhân
- MSSV:A2202603723
- Email trường (không bắt buộc, repo có thể để public):
- Tên nhóm:G2
- Link repo nhóm:https://github.com/trdphat/K5-L3B-Day02-G2-DiscoveryProblemFraming/tree/main

--- 

## 2. Scan problem (CP1)

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

| # | Lăng kính | Job Story: Khi… tôi muốn… để… | Ai chịu ảnh hưởng? | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng) |
|---:|---|---|---|---|
| 1 |Pain từ người khác |Khi tiếp nhận một vụ việc pháp lý, tôi muốn nhanh chóng tra cứu các văn bản pháp luật và xác định điều khoản liên quan để giảm thời gian nghiên cứu và đảm bảo căn cứ pháp lý chính xác.  |Luật sư | Ước tính 30p cho 1 lượt tra cứu |
| 2 | Tốn thời gian|Khi rà soát hợp đồng, tôi muốn nhanh chóng phát hiện các điều khoản bất lợi, thiếu sót hoặc tiềm ẩn rủi ro pháp lý để giảm thời gian kiểm tra và bảo vệ quyền lợi khách hàng. |Luật sư doanh nghiệp |Ước tính 30p đến 1 tiếng cho một hợp đồng |
| 3 | Lặp lại|Khi có văn bản pháp luật mới ban hành, tôi muốn tự động theo dõi và tổng hợp các thay đổi quan trọng để kịp thời cập nhật cho luật sư và khách hàng. | Chuyên viên nghiên cứu pháp lý| Ước tính 30p-60p mỗi ngày để kiểm tra và tổng hợp |
| 4 | Tốn thời gian |Khi khách hàng muốn biết tiến độ xử lý vụ việc, tôi muốn cung cấp thông tin trạng thái hồ sơ nhanh chóng để giảm thời gian liên hệ và chờ phản hồi. |Khách hàng, trợ lý luật sư |10 phút cho 1 lần liên hệ |
| 5 |Lặp lại |	Khi nhận CCCD và giấy đăng ký kinh doanh từ khách hàng, tôi muốn tự động trích xuất tên, mã số và địa chỉ để giảm thời gian nhập liệu. |Trợ lý luật sư |10p cho mỗi lần nhập liệu |
| 6 | Tốn thời gian |Khi nhận hợp đồng từ khách hàng, tôi muốn tự động tìm các thông tin quan trọng như thời hạn, giá trị và ngày hết hạn để không phải đọc toàn bộ hợp đồng. |Chuyên viên pháp lý |Khoảng 10p/hợp đồng |
| 7 |Tốn thời gian |Khi nhận nhiều email từ cùng một khách hàng, tôi muốn tổng hợp các yêu cầu và tài liệu đính kèm để tránh bỏ sót công việc. |Trợ lý luật sư |15-20p để tổng hợp chuỗi email |
| 8 |Pain từ người khác |Khi khách hàng gửi ảnh giấy tờ bị mờ hoặc thiếu trang, tôi muốn phát hiện vấn đề trước khi chuyển hồ sơ cho luật sư để hạn chế yêu cầu gửi lại.|Trợ lý luật sư và khách hàng |5p/bộ hồ sơ  |

**Nếu có dùng AI để gợi ý thêm:** ý nào AI gợi ý mà bạn giữ lại, ý nào bỏ và vì sao.

- Tổng hợp toàn bộ các email yêu cầu và tài liệu đính kèm của khách hàng.
- Trích xuất thông tin quan trọng từ hợp đồng.
---Gợi ý của AI bị loại bỏ:
Chatbot tư vấn pháp lý tự động: Phạm vi quá rộng, yêu cầu độ chính xác pháp lý cao và tiềm ẩn rủi ro cung cấp thông tin sai.
## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 |#5 – Trích xuất thông tin CCCD và giấy đăng ký kinh doanh|Công việc lặp lại, dữ liệu đầu vào/đầu ra rõ ràng, dễ triển khai OCR và đo lường hiệu quả. |Chất lượng ảnh đầu vào, độ chính xác OCR và khả năng tích hợp hệ thống nội bộ.|
| 2 |#6 – Trích xuất thông tin quan trọng từ hợp đồng |Phạm vi nhỏ, tập trung vào các trường như thời hạn, giá trị và ngày hết hạn.  | Hợp đồng có nhiều định dạng, thông tin có thể nằm ở nhiều điều khoản khác nhau.|
| 3 |#7 – Tổng hợp chuỗi email khách hàng|Giảm thời gian đọc email, hỗ trợ tổng hợp yêu cầu và hạn chế bỏ sót công việc. | khả năng truy cập email, bảo mật dữ liệu khách hàng và độ chính xác khi tổng hợp.|

### Problem Card #1

| Trường | Nội dung |
|---|---|
| Job Story | Khi nhận CCCD và giấy đăng ký kinh doanh từ khách hàng, tôi muốn tự động trích xuất tên, mã số và địa chỉ để giảm thời gian nhập liệu. |
| Actor |Trợ lý luật sư |
| Thời điểm / bối cảnh | Khi tiếp nhận hồ sơ và tạo thông tin khách hàng mới trên hệ thống. |
| Quy trình hiện tại (3–7 bước) |1. Nhận giấy tờ → 2. Đọc thông tin → 3. Nhập dữ liệu thủ công → 4. Kiểm tra → 5. Lưu hồ sơ. |
| Bottleneck (bước nào, mất bao nhiêu phút) |Bước 2–3, ước tính hơn 7 phút/bộ hồ sơ. |
| Impact (nếu không giải thì sao) |Tốn thời gian nhập liệu, dễ xảy ra sai sót thông tin và làm chậm quá trình tiếp nhận hồ sơ. |
| Success metric (baseline → target) | Thời gian nhập liệu: 10 phút → dưới 3 phút/bộ hồ sơ.|
| Phương án không dùng AI |Chuẩn hóa biểu mẫu nhập liệu và sử dụng quy tắc kiểm tra định dạng thông tin. |
| Giả thuyết về AI (nếu có) |Sử dụng OCR trích xuất thông tin từ ảnh/PDF, kết hợp kiểm tra dữ liệu và nhân viên xác nhận trước khi lưu. |
| Cảm nhận nhanh | Workflow |

Quy trình nháp hiện tại:
```text
Khách hàng gửi giấy tờ -->Trợ lý tiếp nhận hồ sơ--> Đọc thông tin--> Nhập dữ liệu thủ công-->Thông tin đúng? -->Có [Lưu hồ sơ]-->Không [Chỉnh sửa thông tin]
```

### Problem Card #2

| Trường | Nội dung |
|---|---|
| Job Story | Khi nhận hợp đồng từ khách hàng, tôi muốn tự động tìm các thông tin quan trọng như thời hạn, giá trị và ngày hết hạn để giảm thời gian đọc và tổng hợp. |
| Actor |Chuyên viên pháp lý |
| Thời điểm / bối cảnh |Khi tiếp nhận hợp đồng cần kiểm tra thông tin hoặc theo dõi thời hạn. |
| Quy trình hiện tại (3–7 bước) |1. Nhận hợp đồng → 2. Đọc tài liệu → 3. Tìm điều khoản liên quan → 4. Ghi lại thông tin → 5. Kiểm tra kết quả.  |
| Bottleneck (bước nào, mất bao nhiêu phút) |Bước 2–4, ước tính 8 phút/hợp đồng. |
| Impact (nếu không giải thì sao) |Tốn thời gian tìm kiếm|
| Success metric (baseline → target) |Thời gian trích xuất: 10 phút → dưới 3 phút/hợp đồng |
| Phương án không dùng AI |Sử dụng mẫu hợp đồng chuẩn, tìm kiếm từ khóa và biểu thức chính quy để xác định thông tin |
| Giả thuyết về AI (nếu có) |Sử dụng LLM trích xuất thông tin từ hợp đồng thành JSON, kèm đoạn văn bản nguồn để chuyên viên đối chiếu. |
| Cảm nhận nhanh | Workflow|

Quy trình nháp hiện tại:

```text
    A[Khách hàng gửi hợp đồng] --> B[Chuyên viên tiếp nhận]
    B --> C[Đọc nội dung hợp đồng]
    C --> D[Tìm thời hạn, giá trị, ngày hết hạn]
    D --> E[Ghi lại thông tin]
    E --> F{Đủ thông tin?}
    F -->|Có| G[Kiểm tra và tổng hợp]
    F -->|Không| H[Tìm thông tin bổ sung]
    H --> E
```

### Problem Card #3

| Trường | Nội dung |
|---|---|
| Job Story | Khi nhận nhiều email từ cùng một khách hàng, tôi muốn tổng hợp các yêu cầu và tài liệu đính kèm để tránh bỏ sót công việc.|
| Actor |Trợ lý luật sư |
| Thời điểm / bối cảnh |Khi khách hàng trao đổi nhiều lần qua email về cùng một vụ việc. |
| Quy trình hiện tại (3–7 bước) |1. Mở chuỗi email → 2. Đọc từng email → 3. Kiểm tra tài liệu đính kèm → 4. Ghi lại yêu cầu → 5. Tổng hợp và chuyển luật sư.. |
| Bottleneck (bước nào, mất bao nhiêu phút) |Bước 2–4, ước tính 15 phút/chuỗi email. |
| Impact (nếu không giải thì sao) |Dễ bỏ sót yêu cầu, trùng lặp công việc hoặc phản hồi chậm cho khách hàng. |
| Success metric (baseline → target) | Thời gian tổng hợp: 20 phút → dưới 5 phút/chuỗi email.|
| Phương án không dùng AI |Sử dụng nhãn email, bộ lọc theo khách hàng và checklist theo dõi công việc. |
| Giả thuyết về AI (nếu có) |Sử dụng LLM tổng hợp email, liệt kê yêu cầu, tài liệu đính kèm và công việc cần xử lý, kèm tham chiếu email nguồn.|
| Cảm nhận nhanh | Workflow |

Quy trình nháp hiện tại:

```text
    A[Khách hàng gửi email] --> B[Trợ lý mở chuỗi email]
    B --> C[Đọc từng email]
    C --> D[Kiểm tra tài liệu đính kèm]
    D --> E[Ghi lại yêu cầu]
    E --> F{Đã xem hết email?}
    F -->|Chưa| C
    F -->|Rồi| G[Tổng hợp yêu cầu]
    G --> H[Chuyển luật sư]
```

### Card muốn pitch nhất

- Card số 1 :Trích xuất thông tin CCCD và giấy đăng ký kinh doanh.
- Vì sao: Đây là công việc lặp lại, có đầu vào và đầu ra rõ ràng, phạm vi triển khai nhỏ và dễ đo lường hiệu quả. Có thể ứng dụng OCR để giảm thời gian nhập liệu thủ công, hạn chế sai sót và hỗ trợ trợ lý luật sư xử lý hồ sơ nhanh hơn.
- Câu hỏi muốn nhóm phản biện:Nếu hệ thống OCR vẫn cần nhân viên kiểm tra lại toàn bộ thông tin, liệu giải pháp này có thực sự tiết kiệm thời gian hơn so với nhập liệu thủ công?

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|Ảnh giấy tờ kém chất lượng có thể làm giảm độ chính xác OCR, tăng thời gian sửa lỗi.| Đồng ý|Bổ sung bước kiểm tra chất lượng ảnh đầu vào trước khi trích xuất.|
|OCR chưa chắc tiết kiệm thời gian nếu nhân viên vẫn phải kiểm tra và chỉnh sửa kết quả nhận dạng. | Đồng ý |Bổ sung bước kiểm tra của nhân viên và đề xuất đo tổng thời gian xử lý để so sánh với nhập liệu thủ công.|

---

## 4. Tôi đã tham gia phần nào (CP3 → CP7)

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch Problem Card | | |
| Phản biện bài của bạn khác | Câu hỏi tôi đã đặt: | |
| Nhận phản biện | Câu hỏi tôi nhận được: | Tôi đã sửa gì: |
| Gom cluster / cây OST | | |
| Chọn candidate problem | | |
| Kiểm chứng / research | | |
| Quy trình nhóm | | |
| Problem Statement | | |
| Mức can thiệp AI | | |
| Quyết định | | |


| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch Problem Card | Em đề xuất 3 candidate: #10 — Trích xuất thông tin CCCD và giấy đăng ký kinh doanh; #11 — Trích xuất thông tin hợp đồng; #12 — Tổng hợp yêu cầu từ email khách hàng. | Bổ sung 3 bài toán thuộc lĩnh vực pháp lý để nhóm thảo luận. Candidate #10 được đưa vào shortlist. |
| Phản biện bài của bạn khác | Em đặt câu hỏi về nguy cơ bỏ sót gian lận khi ưu tiên sai cảnh báo (#1), cách phát hiện lỗi tóm tắt tài liệu (#5) và tiêu chí xác định độ khó bài tập (#9). | Giúp nhóm xem xét các rủi ro và hạn chế của những candidate này. |
| Nhận phản biện | Em nhận được 3 câu hỏi về hiệu quả tiết kiệm thời gian của OCR (#10), cách xác định đúng ngày hết hạn hợp đồng (#11) và cách xử lý email có yêu cầu thay đổi liên tục (#12). Em đề xuất bổ sung bước kiểm tra thông tin sau OCR, đối chiếu ngữ cảnh hợp đồng và xác định yêu cầu mới nhất trong chuỗi email. | |
| Gom cluster / cây OST |Em phân tích 3 candidate #10, #11, #12, đối chiếu với các cluster của nhóm và hỗ trợ tổng hợp cây OST, phân biệt Opportunity với Solution. | Nhóm phân 12 candidate thành 3 cluster và xây dựng cây OST gồm Outcome, Opportunity và Solution. |
| Chọn candidate problem | | Nhóm chọn Candidate #1 — Ưu tiên cảnh báo giao dịch đáng ngờ, đạt 31/35 điểm. |
| Kiểm chứng / research | | |
| Quy trình nhóm | | |
| Problem Statement | | |
| Mức can thiệp AI | | |
| Quyết định | | |
---

## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP1 Scan | | | | |
| CP2 Problem Card | | | | |
| CP4 Research | | | | |
| CP5 Quy trình | | | | |
| CP5–6 Problem Statement | | | | |
| CP6 Mức can thiệp / quyết định | | | | |

---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5). **Không dùng AI để viết thay.**

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**

**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**

**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**

**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**

**6.5. Điều khó nhất khi viết Problem Statement là gì?**

**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**

**6.7. Hiểu bài:** giải thích bằng 5–8 câu, không nhìn tài liệu, chuỗi *problem → quy trình → metric → boundary → mức can thiệp AI → quyết định* của bài nhóm mình.

---

## 7. Tài liệu tham khảo

-
