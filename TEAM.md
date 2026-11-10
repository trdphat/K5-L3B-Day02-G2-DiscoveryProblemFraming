# Team

## Thông tin nhóm

- **Tên nhóm:** G2
- **Candidate problem nhóm chọn:** Ưu tiên cảnh báo giao dịch đáng ngờ, giúp Fraud Analyst xác định các giao dịch rủi ro cao cần kiểm tra trước.
- **Quyết định cuối:** Not Yet

## Thành viên

| STT | Họ và tên | MSSV | Vai trò trong nhóm | Tài khoản GitHub |
|---:|---|---|---|---|
| 1 | Trương Đức Phát | | Điều phối nhóm, hội tụ vấn đề, phụ trách research | TruongDucPhat |
| 2 | Đào Nguyễn Quang Thành | | Phân tích và xây dựng quy trình Before/After | DaoNguyenQuangThanh |
| 3 | Hồ An Lộc | 2A202603743 | Phụ trách kiểm chứng, Problem Statement và Success Metric | hoanloc |
| 4 | Nguyễn Minh Nhân | A2202603723 | Phản biện, phân tích mức can thiệp AI, AI Canvas và đánh giá rủi ro | nguyenminhnhan |

## Phân công theo checkpoint

| Checkpoint | Người chính | Người hỗ trợ | Sản phẩm |
|---|---|---|---|
| CP3 — Hội tụ nhóm | Trương Đức Phát | Thành, Lộc, Nhân | Cluster, cây OST, bảng chấm điểm |
| CP4 — Kiểm chứng | Hồ An Lộc | Phát, Thành, Nhân | Assumption Map, Interview Snapshots |
| CP4 — Research | Trương Đức Phát | Nhân, Lộc, Thành | Bảng research có link |
| CP5 — Quy trình trước/sau | Đào Nguyễn Quang Thành | Nhân, Phát, Lộc | Quy trình + bảng Before/After |
| CP5 — Problem Statement v0 | Hồ An Lộc | Nhân, Thành, Phát | Problem Statement v0 |
| CP6 — Mức can thiệp + Problem Statement v1 | Nguyễn Minh Nhân, Hồ An Lộc | Phát, Thành | Ma trận, AI Canvas, Eval, Problem Statement v1 |
| CP6 — Quyết định | Nguyễn Minh Nhân | Phát, Lộc, Thành | 4 rủi ro + Not Yet |

## Cá nhân

### NguyenMinhNhan-A2202603723

**Phần việc phụ trách:**

- Đề xuất và phản biện các Candidate Problem.
- Phân tích mức can thiệp AI, xây dựng AI Canvas và đánh giá theo Google PAIR.
- Tham gia góp ý về Boundary, fallback và đánh giá rủi ro của giải pháp.

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):

- Đề xuất ba Candidate Problem: trích xuất thông tin CCCD và giấy đăng ký kinh doanh (#10), trích xuất thông tin hợp đồng (#11), tổng hợp yêu cầu từ email khách hàng (#12).
- Phản biện nguy cơ bỏ sót gian lận khi ưu tiên sai cảnh báo (#1), độ chính xác khi tóm tắt tài liệu (#5) và tiêu chí đánh giá độ khó bài tập (#9).
- Tham gia đánh giá Candidate #10, phân tích hạn chế của OCR khi kết quả vẫn cần kiểm tra thủ công.
- Góp ý quy trình Rule + ML + Fraud Analyst, đặc biệt là giới hạn tự động hóa và phương án fallback.
- So sánh No AI, Rule, Workflow và Agent; tham gia xây dựng AI Canvas và phân tích hai câu hỏi Google PAIR.
- Góp ý về Boundary, AI intervention point và tiêu chí an toàn trong Problem Statement v1.
- Tham gia đánh giá bốn nhóm rủi ro Value, Usability, Feasibility, Viability và đề xuất quyết định Not Yet.

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):

- `group_report.md` — Mục 2.1: Đề xuất Candidate #10, #11, #12 và phản biện Candidate #1, #5, #9.
- `group_report.md` — Mục 2.4: Tham gia đánh giá Candidate #10 trong bảng shortlist.
- `group_report.md` — Mục 4.2: Góp ý về Boundary, phân chia trách nhiệm giữa Rule, ML, Fraud Analyst và cơ chế fallback.
- `group_report.md` — Mục 6.1–6.4: Phân tích mức can thiệp AI, so sánh No AI, Rule, Workflow, Agent, tham gia xây dựng AI Canvas và đánh giá theo Google PAIR.
- `group_report.md` — Mục 7: Góp ý về Boundary, AI intervention point và tiêu chí an toàn trong Problem Statement v1.
- `group_report.md` — Mục 8: Tham gia đánh giá bốn nhóm rủi ro và đề xuất quyết định Not Yet.
- `report/individual/A2202603723_NguyenMinhNhan.md` — Mục 4: Mô tả chi tiết các đóng góp cá nhân.

**Điều mình học được từ phần nhóm:**

- Em học được rằng cần hiểu rõ vấn đề thực tế trước khi lựa chọn giải pháp. Không phải bài toán nào cũng cần AI hoặc ML, vì đôi khi Rule-based đã có thể đáp ứng nhu cầu. Vì vậy, cần kiểm chứng hiệu quả, đánh giá rủi ro và xác định rõ trách nhiệm của con người trước khi quyết định triển khai.

### HoAnLoc-2A202603743

**Phần việc phụ trách:**

- Phụ trách kiểm chứng, rà soát giả định và xây dựng Success Metric.
- Hoàn thiện Problem Statement v0 và v1, xác định Boundary và AI intervention point.
- Tham gia xây dựng tiêu chí đánh giá chất lượng ưu tiên cảnh báo và điều kiện đánh giá prototype.

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):

- Đóng góp 3 Problem Card cá nhân (#4, #5, #6), trong đó Candidate #5 lọt vào shortlist của nhóm.
- Tham gia rà soát Assumption Map, lưu ý nhóm không coi các số liệu giả định là kết quả đã kiểm chứng thực tế.
- Góp ý phân biệt thời gian sàng lọc tự động (≤10 giây) với thời gian kiểm tra của Fraud Analyst (≤170 giây toàn quy trình).
- Trực tiếp hoàn thiện Problem Statement v0 và v1 với đầy đủ Actor, Bottleneck, Impact, Success Metric có baseline/target định lượng và tiêu chí an toàn (Recall@K tăng ≥5 điểm phần trăm, giữ 100% cảnh báo khi fallback).
- Tham gia thảo luận 4 nhóm rủi ro và thống nhất ngưỡng dừng cho quyết định Not Yet.

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):

- `group_report.md` — Mục 2.1 & 2.4: Đề xuất Candidate #4, #5, #6 và tham gia chấm điểm shortlist.
- `group_report.md` — Mục 3.1: Rà soát Assumption Map và các giới hạn kiểm chứng.
- `group_report.md` — Mục 4.2 & 4.3: Góp ý phân chia thời gian quy trình và bảng Before/After.
- `group_report.md` — Mục 5 & Mục 7: Hoàn thiện Problem Statement v0, v1 và bảng tiêu chí đánh giá đầu ra AI (Recall@K, p95 ≤10 giây, fallback).
- `group_report.md` — Mục 8.2: Tham gia xây dựng ngưỡng dừng thử nghiệm và quyết định Not Yet.
- `report/individual/2A202603743_HoAnLoc.md` — Báo cáo cá nhân đầy đủ của Hồ An Lộc.

**Điều mình học được từ phần nhóm:**

- Em học được cách tư duy từ quy trình thực tế của con người trước khi nghĩ đến công nghệ. Việc đặt ra các chỉ số đo lường định lượng và tiêu chí an toàn nghiêm ngặt (như ngưỡng dừng, cơ chế fallback) giúp nhóm tránh rơi vào bẫy "thần thánh hóa AI" và đưa ra quyết định Not Yet một cách có trách nhiệm và thực tế.