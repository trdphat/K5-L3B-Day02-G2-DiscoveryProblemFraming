# Báo cáo nhóm — Day 02 Discovery & Problem Framing

> Bản chung của nhóm, viết trên repo do nhóm trưởng fork. Không copy file này sang repo cá nhân.
> Template chi tiết và prompt mẫu: [docs/01-worksheet.md](../../docs/01-worksheet.md). Bài mẫu: [docs/02-deliverable-example.md](../../docs/02-deliverable-example.md).

## 1. Thông tin nhóm

- Tên nhóm:G2
- Thành viên: xem `TEAM.md`
- Candidate problem được chọn (1 câu):
- Quyết định cuối: Go / Not Yet / No-Go

---

## 2. Hội tụ nhóm (CP3)

### 2.1. Pitch

| # | Người đưa ra | Candidate (Job Story ngắn) | Actor | Bottleneck | Câu hỏi phản biện nhận được (ai hỏi) |
|---:|---|---|---|---|---|
| 1 | TruongDucPhat | Khi có nhiều cảnh báo giao dịch đáng ngờ, tôi muốn ưu tiên giao dịch rủi ro cao để giảm thời gian kiểm tra và tránh bỏ sót gian lận. | Fraud Analyst, Fraud Operations Team | Bước 4–5: 5 phút/cảnh báo; 500 cảnh báo/ngày tương đương 41,7 giờ công. | Nếu ưu tiên sai, liệu có bỏ sót giao dịch gian lận thật không? — NguyenMinhNhan |
| 2 | TruongDucPhat | Khi khách hàng gửi yêu cầu hoặc khiếu nại, tôi muốn ticket được phân loại và chuyển đúng bộ phận để giảm thời gian chờ xử lý. | Customer Support Agent, Customer Support Supervisor và khách hàng | Bước 3–5: 3 phút/ticket; 2.000 ticket/ngày tương đương 100 giờ công. | Nếu khách hàng mô tả vấn đề không rõ ràng thì phân loại ticket thế nào? — HoAnLoc |
| 3 | TruongDucPhat | Khi chuyển tiền đến tài khoản có dấu hiệu lừa đảo, tôi muốn nhận cảnh báo kịp thời để tránh mất tiền. | Khách hàng sử dụng ứng dụng Fintech; Risk/Fraud Team hỗ trợ kiểm soát rủi ro | Bước 3: thiếu tín hiệu nhận diện tài khoản lừa đảo. Bước 6: tiếp nhận và xác minh ban đầu ước tính 15–30 phút/vụ sau khi tiền đã chuyển. | Nếu cảnh báo nhầm quá nhiều, khách hàng có còn tin vào hệ thống không? — DaoNguyenQuangThanh |
| 4 | HoAnLoc | Khi chuẩn bị tuần học mới, tôi muốn tổng hợp lịch học và deadline để ưu tiên công việc và tránh bỏ sót bài tập. | Sinh viên năm 4, học khoảng 5 môn | Bước 2: tìm thông báo trong nhóm chat mất 10–15 phút/lần, có nguy cơ bỏ sót. | Nếu thông báo chỉ nằm trong nhóm chat thì hệ thống lấy thông tin bằng cách nào? — TruongDucPhat |
| 5 | HoAnLoc | Khi làm bài tập lớn hoặc nghiên cứu, tôi muốn nắm nội dung chính, phương pháp và kết quả từ nhiều tài liệu để chọn thông tin phù hợp. | Sinh viên năm 4, làm bài cá nhân hoặc nghiên cứu nhóm | Bước 3: đọc phương pháp và kết quả mất 20–30 phút/tài liệu, lặp lại với 5–7 tài liệu. | Nếu AI tóm tắt sai kết quả nghiên cứu thì làm sao phát hiện? — NguyenMinhNhan |
| 6 | HoAnLoc | Khi làm bài tập nhóm, tôi muốn theo dõi tiến độ từng thành viên để tổng hợp và nộp bài đúng hạn. | Thành viên nhóm 4–5 người, phụ trách tổng hợp bài | Bước 2: hỏi tiến độ khoảng 15 phút, phải nhắc 2–3 lần; thời gian chờ có thể kéo dài. | Nếu thành viên không cập nhật tiến độ thì hệ thống có giải quyết được vấn đề không? — DaoNguyenQuangThanh |
| 7 | DaoNguyenQuangThanh | Khi nhận nhiệm vụ mới, tôi muốn tìm lại thông tin từ chat, tài liệu và cuộc họp để hiểu bối cảnh, tránh hỏi lại hoặc làm sai. | Sinh viên đại học đang thực tập | Bước 2–4: tìm và đối chiếu thông tin mất 15–30 phút/lần; chưa xác định nguồn tốn thời gian nhất. | Nếu thông tin trong chat và tài liệu mâu thuẫn nhau thì nên tin nguồn nào? — HoAnLoc |
| 8 | DaoNguyenQuangThanh | Khi nghỉ học, tôi muốn tổng hợp nội dung bài giảng và bài tập đã bỏ lỡ để theo kịp lớp. | Sinh viên vừa học vừa thực tập | Bước 1–3: hỏi bạn, xin ghi chú và xem tài liệu; tổng quy trình mất 30–60 phút/buổi, chưa xác định bottleneck riêng. | Nếu không có ghi chú hoặc tài liệu buổi học thì AI lấy gì để tổng hợp? — TruongDucPhat |
| 9 | DaoNguyenQuangThanh | Khi nhận đề cương ôn tập, tôi muốn xác định các dạng bài trung bình–khó để ưu tiên ôn luyện. | Sinh viên chuẩn bị thi nhiều môn | Bước 3–4: tìm bài tập và ước lượng độ khó; tổng thời gian 30–45 phút/đề cương, chưa đo riêng từng bước. | Độ khó bài tập tùy năng lực mỗi người, vậy dựa vào đâu để phân loại? — NguyenMinhNhan |
| 10 | NguyenMinhNhan | Khi nhận CCCD và giấy đăng ký kinh doanh, tôi muốn trích xuất tên, mã số và địa chỉ để giảm thời gian nhập liệu. | Trợ lý luật sư | Bước 2–3: ước tính hơn 7 phút/bộ hồ sơ. | Nếu OCR vẫn cần kiểm tra lại toàn bộ thông tin thì có thực sự tiết kiệm thời gian không? — HoAnLoc |
| 11 | NguyenMinhNhan | Khi nhận hợp đồng, tôi muốn trích xuất thời hạn, giá trị và ngày hết hạn để giảm thời gian đọc và tổng hợp. | Chuyên viên pháp lý | Bước 2–4: ước tính 8 phút/hợp đồng. | Nếu hợp đồng có nhiều ngày tháng khác nhau thì làm sao xác định đúng ngày hết hạn? — DaoNguyenQuangThanh |
| 12 | NguyenMinhNhan | Khi nhận nhiều email từ một khách hàng, tôi muốn tổng hợp yêu cầu và tài liệu đính kèm để tránh bỏ sót công việc. | Trợ lý luật sư | Bước 2–4: ước tính 15 phút/chuỗi email. | Nếu email có nhiều yêu cầu thay đổi liên tục thì làm sao tránh tổng hợp sai? — TruongDucPhat |

### 2.2. Cluster

| Cluster | Các candidate | Pattern chung |
|---|---|---|
| **A — Xử lý và phân loại thông tin** | #1, #2, #3, #9, #10, #11 | Cần kiểm tra, phân loại hoặc trích xuất thông tin để đưa ra quyết định nhanh và chính xác hơn, giảm thao tác thủ công. |
| **B — Tìm kiếm và tổng hợp thông tin** | #5, #7, #8, #12 | Thông tin nằm rải rác trong nhiều tài liệu, email hoặc nguồn khác nhau, khiến người dùng mất thời gian tìm kiếm, đọc và tổng hợp. |
| **C — Theo dõi và quản lý công việc** | #4, #6 | Khó theo dõi lịch trình, deadline và tiến độ công việc, dễ bỏ sót hoặc chậm hoàn thành nhiệm vụ. |

### 2.3. Opportunity Solution Tree rút gọn

```text
OUTCOME: Giảm thời gian xử lý công việc thủ công và hạn chế sai sót thông tin.

├── Opportunity A: Mất nhiều thời gian kiểm tra,
│   phân loại và trích xuất thông tin.
│   │
│   ├── Solution A1: Ưu tiên cảnh báo giao dịch
│   │   bằng rule-based hoặc ML Risk Scoring.
│   │
│   └── Solution A2: Dùng OCR để hỗ trợ
│       trích xuất thông tin giấy tờ.
│
├── Opportunity B: Khó tìm kiếm và tổng hợp
│   thông tin từ nhiều nguồn khác nhau.
│   │
│   └── Solution B1: Công cụ tìm kiếm và
│       tóm tắt tài liệu.
│
└── Opportunity C: Khó theo dõi lịch trình,
    deadline và tiến độ công việc.
    │
    └── Solution C1: Công cụ tổng hợp lịch
        và nhắc deadline.

```
Nhóm ưu tiên xem xét Opportunity A vì các bài toán trong nhóm này có quy trình xử lý tương đối rõ và dễ xác định điểm nghẽn. Trong đó, Candidate #1 liên quan đến việc Fraud Analyst phải kiểm tra nhiều cảnh báo giao dịch, nên nhóm đưa vào shortlist để đánh giá tiếp.

Các ý như dùng OCR hoặc LLM để trích xuất thông tin, xây dựng công cụ tóm tắt tài liệu và ứng dụng nhắc deadline được chuyển xuống tầng Solution thay vì xem là Opportunity. Đây mới là các hướng giải quyết ban đầu, nhóm chưa lựa chọn giải pháp triển khai chính thức.

### 2.4. Chấm điểm shortlist (1–5)
| Candidate | Actor rõ | Quy trình rõ | Pain có bằng chứng | Impact đo được | Vừa sức lab | So sánh được No AI/Rule/Workflow/Agent | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| #1 — Ưu tiên cảnh báo giao dịch đáng ngờ | 5 | 5 | 2 | 5 | 4 | 5 | 5 | **31** |
| #5 — Đọc và tổng hợp tài liệu nghiên cứu | 5 | 5 | 3 | 4 | 4 | 4 | 5 | **30** |
| #10 — Trích xuất thông tin CCCD và giấy đăng ký kinh doanh | 5 | 5 | 2 | 5 | 5 | 4 | 3 | **29** |

**Candidate được chọn:** #1 — Ưu tiên cảnh báo giao dịch đáng ngờ.

**Vì sao chọn:** Nhóm chọn #1 vì bài toán xác định được đối tượng sử dụng, các bước xử lý và điểm nghẽn cần cải thiện. Nhóm cũng có thể dùng dữ liệu giao dịch giả lập để so sánh cách xử lý thủ công, rule-based và ML Risk Scoring. Kết quả có thể đánh giá qua thời gian xử lý, khả năng ưu tiên cảnh báo và tỷ lệ phát hiện gian lận.

**Vì sao loại các candidate còn lại:**
- **#5:** Bài toán gần gũi với sinh viên và dễ tìm dữ liệu để thử nghiệm. Tuy nhiên, nhóm nhận thấy việc đánh giá bản tóm tắt có chính xác và đầy đủ hay không sẽ cần thêm công sức kiểm tra thủ công.
- **#10:** Bài toán phù hợp để thử nghiệm OCR, nhưng nhóm lo ngại việc nhận diện sai thông tin trên giấy tờ có thể khiến người dùng phải kiểm tra lại nhiều lần. Ngoài ra, nhóm cần chuẩn bị dữ liệu thử nghiệm không chứa thông tin cá nhân thật.

**Xử lý bất đồng (nếu có):** Nhóm không có bất đồng lớn khi lựa chọn. Do điểm số của ba candidate khá sát nhau, nhóm trao đổi thêm về khả năng thử nghiệm và cách đánh giá hiệu quả trước khi thống nhất chọn #1.

## 3. Kiểm chứng + research giải pháp đã có (CP4)

### 3.1. Assumption Map

| # | Giả định | Loại (Value / Usability / Feasibility / Viability) | Quan trọng (1–5) | Đã có bằng chứng (1–5) | Kiểm chứng trước? |
|---:|---|---|---:|---:|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |
| 4 | | | | | |
| 5 | | | | | |
| 6 | | | | | |

*Điền 4–6 giả định; xóa dòng thừa.*

Giả định nhóm kiểm chứng trong buổi này:

### 3.2. Kiểm chứng

Cách đã dùng: Phỏng vấn / Survey / Log, ticket, review

Interview snapshot (mỗi buổi phỏng vấn một bảng, hoặc đặt file trong `report/assets/cp4-interview-snapshot-N.md`):

| Trường | Nội dung |
|---|---|
| Người được hỏi (vai trò, không ghi tên thật) | |
| Câu nói đáng nhớ nhất (nguyên văn) | |
| Lần gần nhất gặp vấn đề này: chuyện gì đã xảy ra? | |
| Hiện đang xử lý bằng cách nào (workaround)? | |
| Mất bao lâu, bao lần? | |
| Insight / opportunity rút ra | |

Tổng hợp:

| Nguồn | Số người / số mẫu | Tín hiệu xác nhận | Tín hiệu phản bác |
|---|---:|---|---|
| | | | |

**Nhóm đã sửa problem thế nào sau kiểm chứng:**

### 3.3. Research giải pháp đã có

| Công cụ / case / pattern | Link | Giải bước nào trong quy trình? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
|---|---|---|---|---|---|
| | | | | | |
| | | | | | |
| | | | | | |

---

## 4. Quy trình trước/sau (CP5)

### 4.1. Quy trình hiện tại

Sơ đồ (ASCII, Mermaid hoặc link ảnh trong `report/assets/`):

```text

```

| Bước | Actor | Input | Output | Thời gian / tần suất | Ghi chú |
|---:|---|---|---|---|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |
| 4 | | | | | |
| 5 | | | | | |

**Bottleneck chính:**

### 4.2. Quy trình tương lai

Ghi rõ bước nào **Rule**, bước nào **AI**, bước nào **con người**, **boundary** ở đâu, **phương án quay về** khi AI sai.

```text

```

### 4.3. Before / after

| Chỉ số | Trước | Sau (kỳ vọng) | Ghi chú |
|---|---:|---:|---|
| Số bước | | | |
| Tổng thời gian | | | |
| Số bước thủ công | | | |
| Bottleneck chính | | | |
| Rủi ro mới phát sinh | | | |

---

## 5. Problem Statement v0 (CP5)

| Trường | Nội dung |
|---|---|
| **Actor** | |
| **Quy trình** | |
| **Bottleneck** | |
| **Impact** | |
| **Success Metric** (baseline → target, cách đo) | |
| **Boundary** (AI không được làm gì; khi nào cần con người kiểm tra — HITL) | |

Phản biện nhận được (từ AI hoặc nhóm khác) và nhóm có đồng ý không:

-

---

## 6. Mức can thiệp AI (CP6)

### 6.1. Ma trận độ mơ hồ × độ phức tạp

Bài của nhóm nằm ở ô:

Vì sao:

### 6.2. So sánh 4 mức

| Mức | Phương án cho bài của nhóm | Đủ khi nào | Rủi ro | Chọn? |
|---|---|---|---|---|
| **No AI** (sửa quy trình) | | | | |
| **Rule** | | | | |
| **Workflow** | | | | |
| **Agent** | | | | |

**Mức chọn:**

**Vì sao không chọn mức đơn giản hơn:**

### 6.3. AI Canvas rút gọn

| Thành phần | Nội dung |
|---|---|
| **Prediction** — AI dự đoán / tạo ra gì? | |
| **Judgment** — con người cân nhắc, quyết định gì? | |
| **Action** — hành động cuối cùng là gì, ai làm? | |
| **Outcome** — đo kết quả bằng gì? | |
| **Input** — AI cần dữ liệu đầu vào gì mỗi lần chạy? Có sẵn không? | |
| **Feedback** — lấy phản hồi ở đâu để cải thiện? | |

### 6.4. Hai câu hỏi của Google PAIR

- Người dùng muốn **được hỗ trợ (augment)** hay **giao hẳn việc (automate)**? Bằng chứng:
- AI sai kiểu nào tệ hơn, **báo nhầm** hay **bỏ sót**? Vì sao, và thiết kế đã xử lý thế nào:

---

## 7. Problem Statement v1 + tiêu chí đánh giá (CP6)

| Trường | Nội dung |
|---|---|
| **Actor** | |
| **Quy trình** | |
| **Bottleneck** | |
| **Impact** | |
| **Success Metric** (baseline → target, cách đo) | |
| **Boundary** | |
| **AI intervention point** | |
| **Mức chọn** | No AI / Rule / Workflow / Agent |
| **Rủi ro & người kiểm tra** | |

**Thay đổi so với v0 và lý do:**

| Trường | v0 | v1 | Vì sao đổi |
|---|---|---|---|
| | | | |

**Tiêu chí đánh giá đầu ra của AI (3–5 tiêu chí):**

| # | Tiêu chí | Đạt khi | Không đạt khi |
|---:|---|---|---|
| 1 | | | |
| 2 | | | |
| 3 | | | |

---

## 8. Quyết định (CP6)

### 8.1. Bốn rủi ro

| Rủi ro | Câu hỏi | Mức độ rủi ro (Thấp = an toàn / TB / Cao = nguy hiểm) | Lý do / bằng chứng |
|---|---|---|---|
| **Value** | Người dùng có thật sự cần và sẽ dùng không? | | |
| **Usability** | Người dùng có dùng được, có hiểu và sửa được đầu ra của AI không? | | |
| **Feasibility** | Có đủ dữ liệu, công cụ, kỹ năng để làm không? | | |
| **Viability** | Có hợp chi phí, pháp lý, quy định tổ chức không? Ai vận hành? | | |

### 8.2. Kết luận

**Quyết định:** Go / Not Yet / No-Go

**Lý do:**

**Nếu Go — pilot nhỏ nhất:**

**Nếu Not Yet — cần kiểm chứng gì trước:**

**Nếu No-Go — nên làm gì thay AI:**

**Ngưỡng dừng** (nếu sau … mà … thì quay về …):

---

## 9. Hạn chế và hướng tiếp theo

-

## 10. Tài liệu tham khảo

-