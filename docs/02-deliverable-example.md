# Bài làm mẫu — Báo cáo tuần của Product Manager

> Đây là ví dụ một bài nộp hoàn chỉnh. **Không copy nội dung**, hãy học cách đi: scan → Problem Card → hội tụ → kiểm chứng → quy trình → Problem Statement → mức can thiệp AI → quyết định.
>
> Nhân vật và công ty trong ví dụ là hư cấu. Thông tin về công cụ trong bảng research được kiểm tại thời điểm viết (11/2026); khi bạn làm bài, hãy tự kiểm lại.

**Nhân vật:** Minh, Junior Product Manager ở một công ty SaaS khoảng 50 người, dùng Jira, Google Sheets và Slack gói Pro. Mỗi sáng thứ Hai, Minh tổng hợp số liệu từ ba công cụ này để viết báo cáo tuần cho Engineering Manager (EM) và CEO.

**Vì sao đây là ví dụ tốt:** actor cụ thể; quy trình lặp lại hằng tuần; bottleneck rõ; có baseline thời gian; so sánh được No AI / Rule / Workflow / Agent; và quan trọng nhất, **research làm nhóm đổi kết luận**.

---

# Phần cá nhân (của Minh)

## 2. Scan problem (CP1)

Minh scan 10 problem, vượt mức tối thiểu 5.

| # | Lăng kính | Job Story | Ai chịu ảnh hưởng? | Dấu hiệu thật |
|---:|---|---|---|---|
| 1 | Lặp lại | Khi tới sáng thứ Hai, tôi muốn có số liệu sprint và tình hình team ở một chỗ, để gửi báo cáo tuần cho CEO trước 10h | PM, EM, CEO | Tự bấm giờ 2 tuần gần nhất: 85 và 95 phút |
| 2 | Lặp lại | Khi cập nhật slide cho buổi họp tháng, tôi muốn có sẵn velocity các sprint, để không phải copy tay từ Jira | PM | Mỗi tháng 1 lần, khoảng 20 phút |
| 3 | Tốn thời gian | Khi nhận một PRD 10–15 trang cần review, tôi muốn nắm nhanh các quyết định chính, để comment đúng chỗ trước hạn | PM reviewer, design lead | Khoảng 45 phút/bản, 2 bản/tuần |
| 4 | Tốn thời gian | Khi vừa xong một cuộc họp liên team, tôi muốn có danh sách việc cần làm và người phụ trách, để không ai bỏ sót | PM, team | 30 phút/buổi viết lại ghi chú |
| 5 | Cần đọc, tổng hợp nhiều thông tin | Khi có quá nhiều task cùng hạn, tôi muốn biết nên làm việc nào trước, để không trễ việc quan trọng | PM, team | Tuần trước trễ 2 task vì ưu tiên sai |
| 6 | Cần đọc, tổng hợp nhiều thông tin | Khi cần biết vì sao team từng chọn phương án A, tôi muốn tìm lại được quyết định cũ, để không tranh luận lại từ đầu | Cả team | 10–15 phút mỗi lần tìm trong Slack, 3–4 lần/tuần |
| 7 | Pain từ người khác | Khi designer nhận spec từ tôi, họ muốn hiểu đúng yêu cầu ngay lần đầu, để không phải hỏi lại | Designer, PM | Designer hỏi lại 2–3 lần/spec (đếm từ thread Slack) |
| 8 | Pain từ người khác | Khi CEO cần chuẩn bị họp leadership sáng thứ Hai, CEO muốn có báo cáo trước giờ họp, để nắm tình hình | CEO, PM | 3/8 tuần gần nhất báo cáo gửi trễ |
| 9 | Tốn thời gian | Khi cuối tháng, tôi muốn có KPI từ nhiều dashboard trong một bảng, để báo cáo tháng | PM, manager | Mỗi tháng khoảng 2 tiếng |
| 10 | Lặp lại | Khi tới giờ standup, tôi muốn có sẵn update hôm qua, để không phải nhớ lại | PM | 5–10 phút/ngày |

**AI gợi ý thêm:** sau khi tự scan 8 ý, Minh hỏi AI và giữ lại ý #9 và #10. Bỏ ý "trợ lý AI quản lý toàn bộ dự án" vì quá rộng và không có quy trình thật.

## 3. Top 3 Problem Cards (CP2)

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 | Báo cáo tuần (#1) | Quy trình rõ, tốn thời gian, có baseline đo thật | Narrative "đủ tốt" đo thế nào? |
| 2 | Review PRD (#3) | Pain thật, nhiều người gặp | Chất lượng review khó đo |
| 3 | Tìm quyết định cũ (#6) | Nhiều người đau, impact rộng | Quyền truy cập dữ liệu khó, phạm vi dễ quá rộng |

### Problem Card #1 — Báo cáo tuần

| Trường | Nội dung |
|---|---|
| Job Story | Khi tới sáng thứ Hai, tôi muốn có số liệu sprint và tình hình team ở một chỗ, để gửi báo cáo tuần cho CEO trước 10h |
| Actor | Junior PM phụ trách báo cáo tuần cho EM và CEO |
| Thời điểm / bối cảnh | Sáng thứ Hai, trước buổi họp leadership lúc 10h |
| Quy trình hiện tại | 1. Export dữ liệu sprint từ Jira · 2. Lấy số từ Google Sheets · 3. Đọc lại Slack cả tuần · 4. Tổng hợp vào Google Docs · 5. Viết narrative (điểm nổi bật, rủi ro, việc tiếp theo) · 6. Tự review và format · 7. Gửi email |
| Bottleneck | Bước 5, viết narrative: khoảng 25 phút, hay bị "trang trắng" |
| Impact | 90 phút/tuần cho 1 PM; công ty có 3 PM nên khoảng 270 phút/tuần; 3/8 tuần gần nhất gửi trễ |
| Success metric | Tổng thời gian từ 90 phút xuống dưới 30 phút, số câu hỏi lại từ CEO/EM không tăng |
| Phương án không dùng AI | Template cố định + dashboard Jira + checklist: giảm thời gian format, chưa giảm thời gian viết narrative |
| Giả thuyết về AI | AI soạn nháp narrative từ dữ liệu đã gom; PM review và sửa trước khi gửi |
| Cảm nhận nhanh | Workflow |

```text
HIỆN TẠI — 90 phút

[1 Export Jira: 10'] → [2 Lấy số Sheets: 10'] → [3 Đọc Slack: 15']
→ [4 Tổng hợp Docs: 15'] → [5 Viết narrative: 25'] ← BOTTLENECK
→ [6 Review + format: 10'] → [7 Gửi: 5']
```

Card #2 và #3 (tóm tắt):

| Card | Actor | Bottleneck | Metric | Cảm nhận nhanh |
|---|---|---|---|---|
| Review PRD | PM reviewer | Đọc 10–15 trang để nắm ngữ cảnh | 45 → 20 phút/bản | Workflow |
| Tìm quyết định cũ | Thành viên team | Tìm keyword rồi đọc lại cả thread | 15 → dưới 2 phút/lần | Workflow hoặc Agent |

**AI phản biện card #1:**

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|---|---|---|
| Baseline 90 phút chỉ dựa trên trí nhớ | Đồng ý | Bấm giờ thật 2 tuần: 85 và 95 phút |
| Chưa chắc CEO đọc phần narrative | Đồng ý một phần | Đưa vào danh sách giả định cần kiểm chứng ở CP4 |
| Gợi ý làm agent tự gửi báo cáo | Không đồng ý | Giữ "PM review trước khi gửi" làm boundary |

---

# Phần nhóm

## 2. Hội tụ nhóm (CP3)

Nhóm 4 người, 12 candidate.

### Cluster

| Cluster | Các candidate | Pattern chung |
|---|---|---|
| A — Báo cáo / tổng hợp | Báo cáo tuần, recap họp, báo cáo tiến độ lab | Gom thông tin nhiều nguồn rồi viết lại cho người khác đọc |
| B — Tìm kiếm | Tìm quyết định cũ trong Slack, tìm tài liệu trên LMS, FAQ lab | Tìm đúng thông tin trong nhiều nguồn rời rạc |
| C — Review | Review PRD, kiểm Problem Statement, review bài tập | Đọc bản nháp và chỉ ra thiếu sót |
| D — Theo dõi việc | Theo dõi action item, nhắc deadline | Sau cuộc họp nhiều việc bị rơi |

### Opportunity Solution Tree rút gọn

```text
OUTCOME: Giảm thời gian PM dành cho báo cáo định kỳ mà leadership vẫn đủ thông tin
├── Opportunity: Số liệu nằm rải rác ở 3 công cụ, phải copy tay
├── Opportunity: Viết phần nhận định (điểm nổi bật, rủi ro) mỗi tuần mất nhiều thời gian nhất
└── Opportunity: PM không biết leadership thật sự đọc phần nào
     ✗ "Dashboard tự động"        ← solution, gạch khỏi tầng này
     ✗ "Chatbot viết báo cáo"     ← solution, gạch khỏi tầng này
```

### Chấm điểm shortlist

| Candidate | Actor rõ | Quy trình rõ | Pain có bằng chứng | Impact đo được | Vừa sức lab | So sánh được 4 mức | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Báo cáo tuần | 5 | 5 | 4 | 5 | 5 | 5 | 5 | **34** |
| Review PRD | 4 | 5 | 3 | 3 | 5 | 4 | 4 | 28 |
| Tìm quyết định cũ | 4 | 4 | 4 | 4 | 3 | 4 | 4 | 27 |

**Chọn:** Báo cáo tuần.

**Vì sao loại hai candidate kia:** Tìm quyết định cũ có impact rộng nhưng cần quyền đọc toàn bộ Slack và dễ trượt thành dự án tìm kiếm quá lớn. Review PRD có quy trình rõ nhưng nhóm không thống nhất được cách đo chất lượng review trong thời gian lab.

**Bất đồng:** Lan muốn chọn "Tìm quyết định cũ" vì impact rộng hơn. Nhóm thống nhất ghi nó vào mục "hướng tiếp theo" và chọn bài có baseline đo được ngay.

## 3. Kiểm chứng + research (CP4)

### Assumption Map

| # | Giả định | Loại | Quan trọng | Đã có bằng chứng | Kiểm trước? |
|---:|---|---|---:|---:|---|
| 1 | PM khác cũng mất trên 60 phút/tuần cho báo cáo | Value | 5 | 2 | ✅ |
| 2 | Bước tốn nhất là viết narrative, không phải lấy số | Value | 5 | 2 | ✅ |
| 3 | Leadership đọc phần narrative, không chỉ xem số | Value | 4 | 1 | ✅ |
| 4 | Dữ liệu Jira/Sheets lấy ra được tự động | Feasibility | 4 | 4 | — |
| 5 | Công ty cho phép đưa dữ liệu nội bộ vào công cụ AI | Viability | 5 | 2 | Hỏi EM sau lab |

### Kiểm chứng

Nhóm phỏng vấn 3 PM/PO quen biết (theo The Mom Test) và làm poll 6 người trong lớp.

Interview snapshot — người thứ 2:

| Trường | Nội dung |
|---|---|
| Người được hỏi | PO, công ty fintech khoảng 200 người |
| Câu nói đáng nhớ | "Số thì 5 phút là xong, cái mình ngồi lâu là viết sao cho sếp hiểu tuần này có gì đáng lo." |
| Lần gần nhất | Thứ Sáu tuần trước, viết update tháng, mất khoảng 2 tiếng |
| Workaround hiện tại | Copy báo cáo tháng trước rồi sửa |
| Mất bao lâu, bao lần | Update tuần khoảng 60 phút, update tháng khoảng 2 tiếng |
| Insight | Pain nằm ở phần nhận định, không phải phần lấy số |

Tổng hợp:

| Nguồn | Số mẫu | Tín hiệu xác nhận | Tín hiệu phản bác |
|---|---:|---|---|
| Phỏng vấn | 3 | 2/3 viết update thủ công và đều mất nhiều thời gian nhất ở phần narrative | 1 người nói dashboard Jira đã đủ cho team họ, CEO chỉ xem số |
| Poll trong lớp | 6 | 4/6 từng phải tổng hợp báo cáo từ nhiều nguồn | 2/6 nói template là đủ |

**Nhóm đã sửa problem:** thu hẹp từ "tự động hóa báo cáo tuần" thành "**soạn nháp phần nhận định từ dữ liệu đã có**". Thêm phương án không dùng AI (template + dashboard) cho những team mà leadership chỉ cần số. Giả định #3 vẫn chưa đủ bằng chứng.

### Research giải pháp đã có

| Công cụ / case | Link | Giải bước nào? | Điểm mạnh | Khoảng trống / rủi ro | Bài học |
|---|---|---|---|---|---|
| Atlassian Rovo (AI trong Jira/Confluence) | https://support.atlassian.com/rovo/docs/what-is-rovo/ | Bước 1 + 5: tóm tắt sprint, soạn status update từ dữ liệu Jira | Có sẵn trong Jira, không phải tự xây | Cộng đồng người dùng báo phần **tính số liệu** chưa ổn định; chỉ thấy dữ liệu Jira, không thấy Sheets | Dùng được cho phần chữ, nhưng **số liệu phải lấy bằng rule** và PM phải kiểm |
| AI Executive Status Reports (Aneto, Atlassian Marketplace) | https://marketplace.atlassian.com/apps/1238133/ai-executive-status-reports-for-jira-by-aneto | Bước 1–5: từ bộ lọc JQL + template ra báo cáo cho lãnh đạo | Chuyên đúng việc báo cáo cho lãnh đạo | Thêm chi phí, chỉ dựa trên Jira | Thị trường đã có sản phẩm, **không nên tự xây từ đầu** |
| Template n8n: Jira + AI → báo cáo tuần | https://n8n.io/workflows/9683 | Bước 1–7: lịch chạy, lấy Jira, AI tóm tắt, gửi email | Đúng kiến trúc **Workflow**: các bước định sẵn, AI làm một bước | Tự động gửi email, không có bước người duyệt; cần người biết cấu hình | Mượn kiến trúc, nhưng **thêm bước PM duyệt** trước khi gửi |
| Slack AI | https://slack.com/help/articles/25076892548883-Guide-to-AI-features-in-Slack | Bước 3: tóm tắt thread và kênh | Giảm thời gian đọc Slack | Từ 6/2025, gói Pro chỉ có tóm tắt hội thoại và ghi chú huddle; recap và tìm kiếm AI nằm ở gói Business+ trở lên | Công ty của Minh dùng gói Pro: dùng tóm tắt thread làm input, không trông vào recap |

**Kết luận research:**

```text
Phần lớn quy trình đã có công cụ làm được. Không có lý do tự xây agent.
Hướng hợp lý: Rule lấy số liệu → AI soạn nháp narrative (Rovo hoặc prompt chuẩn) → PM duyệt → PM gửi.
```

Đây là điểm khác lớn nhất so với bản nháp ban đầu của Minh: ban đầu Minh định "xây một công cụ AI viết báo cáo".

## 4. Quy trình trước/sau (CP5)

```text
HIỆN TẠI — 7 bước, 90 phút, 7/7 bước thủ công

[1 Export Jira: 10'] → [2 Lấy số Sheets: 10'] → [3 Đọc Slack: 15']
→ [4 Tổng hợp Docs: 15'] → [5 Viết narrative: 25'] ← BOTTLENECK
→ [6 Review + format: 10'] → [7 Gửi email: 5']

TƯƠNG LAI — 5 bước, khoảng 25 phút, 2/5 bước thủ công

[1 Lấy số Jira + Sheets vào template: 2']   ← RULE (dashboard/script)
→ [2 Tóm tắt thread Slack quan trọng: 3']   ← AI có sẵn trong Slack Pro
→ [3 Soạn nháp narrative: 1']               ← AI (Rovo hoặc prompt chuẩn)
→ [4 PM kiểm số + sửa nháp: 15']            ← CON NGƯỜI
→ [5 PM gửi: 2']                            ← CON NGƯỜI

BOUNDARY: AI không tự gửi, không tự sửa số liệu, chỉ dùng dữ liệu được đưa vào.
PHƯƠNG ÁN QUAY VỀ: nháp kém hoặc sai số → PM bỏ nháp, viết theo template cũ.
```

| Chỉ số | Trước | Sau (kỳ vọng) | Ghi chú |
|---|---:|---:|---|
| Số bước | 7 | 5 | |
| Tổng thời gian | 90' | khoảng 25' | Target chính: dưới 30' |
| Bước thủ công | 7/7 | 2/5 | PM vẫn kiểm và gửi |
| Bottleneck | Viết narrative | PM kiểm + sửa | Bottleneck chấp nhận được vì là điểm kiểm soát chất lượng |
| Rủi ro mới | — | AI bịa nhận định, sai số | Xử lý bằng boundary + tiêu chí đánh giá |

## 5. Problem Statement v0 (CP5)

| Trường | Nội dung |
|---|---|
| **Actor** | Junior PM phụ trách báo cáo tuần cho leadership |
| **Quy trình** | Mỗi sáng thứ Hai: export Jira, lấy số Sheets, đọc Slack, tổng hợp Docs, viết narrative, review, gửi email |
| **Bottleneck** | Viết narrative mất khoảng 25 phút vì phải biến dữ liệu thô thành điểm nổi bật, rủi ro, việc tiếp theo |
| **Impact** | 90 phút/tuần/PM; 3/8 tuần gần nhất gửi trễ; leadership thiếu bối cảnh trước họp |
| **Success Metric** | Tổng thời gian từ 90' (bấm giờ 2 tuần) xuống dưới 30', đo bằng PM tự ghi giờ 4 tuần pilot |
| **Boundary** | AI không tự gửi, không bịa nhận định, không thay PM duyệt |

**Phản biện nhận được:** AI chỉ ra metric chỉ đo tốc độ, không đo chất lượng: báo cáo nhanh hơn nhưng tệ hơn thì sao? Nhóm đồng ý và thêm metric chất lượng ở v1.

## 6. Mức can thiệp AI (CP6)

**Ma trận:** độ mơ hồ **cao** (narrative mỗi tuần mỗi khác, nhiều cách viết đều chấp nhận được), độ phức tạp **thấp–trung bình** (3 nguồn nhưng các bước cố định, không rẽ nhánh). → Workflow có AI ở một bước.

| Mức | Phương án | Đủ khi nào | Rủi ro | Chọn? |
|---|---|---|---|---|
| **No AI** | Template + checklist + gửi trước 9h | Leadership chỉ cần số | Không giảm thời gian viết narrative | Dùng cho team chỉ cần số |
| **Rule** | Dashboard/script tự lấy số vào template | Bước lấy số | Không viết được narrative | **Dùng cho bước 1** |
| **Workflow** | Rule lấy số → AI soạn nháp → PM duyệt → gửi | Các bước cố định, AI chỉ làm phần ngôn ngữ | Nháp sai hoặc nhạt | **Chọn** |
| **Agent** | AI tự tìm nguồn, tự phân tích, tự hỏi thêm, tự gửi | Khi bước tiếp theo không đoán trước được | Quá rộng, nhiều quyền truy cập, khó kiểm soát | Không chọn |

**Vì sao không chọn mức đơn giản hơn:** Phỏng vấn (3 người, mẫu nhỏ) cho thấy 2/3 người vẫn mất nhiều thời gian nhất ở phần narrative, đúng phần mà No AI (template) và Rule (dashboard tự lấy số) không làm được. Người còn lại nói dashboard là đủ, nên với team chỉ cần số, nhóm vẫn khuyến nghị No AI.

**AI Canvas rút gọn:**

| Thành phần | Nội dung |
|---|---|
| Prediction | Bản nháp narrative: 3 điểm nổi bật, rủi ro/blocker, việc tuần tới |
| Judgment | PM quyết định điểm nào đáng báo cáo, rủi ro nào cần nhấn mạnh với CEO |
| Action | PM sửa và gửi email |
| Outcome | Thời gian làm báo cáo; số câu CEO/EM hỏi lại; tỉ lệ nháp phải viết lại |
| Input | Số liệu sprint (Jira), KPI (Sheets), tóm tắt thread Slack, báo cáo tuần trước. Đều có sẵn |
| Feedback | Phần PM sửa trong nháp mỗi tuần; câu hỏi lại của CEO |

**Câu hỏi PAIR:**

- **Augment hay automate?** Augment. 2 người cần phần narrative đều muốn "có bản nháp để sửa"; người còn lại chỉ cần dashboard số. Không ai muốn báo cáo tự gửi đi.
- **Sai kiểu nào tệ hơn?** Bỏ sót rủi ro tệ hơn báo nhầm: CEO không biết blocker thì quyết định sai. Vì vậy tiêu chí đánh giá ưu tiên "không bỏ sót blocker có trong dữ liệu".

## 7. Problem Statement v1 + tiêu chí đánh giá (CP6)

| Trường | Nội dung |
|---|---|
| **Actor** | Junior PM phụ trách báo cáo tuần cho leadership, ở team mà leadership đọc phần narrative |
| **Quy trình** | Lấy số Jira + Sheets → đọc Slack → viết narrative → review → gửi |
| **Bottleneck** | Viết narrative mất khoảng 25 phút |
| **Impact** | 90 phút/tuần/PM; 3/8 tuần gửi trễ |
| **Success Metric** | (1) Thời gian từ 90' xuống dưới 30'; (2) PM phải viết lại dưới 50% bản nháp; (3) số câu CEO/EM hỏi lại không tăng so với 4 tuần trước pilot |
| **Boundary** | AI không tự gửi, không tự sửa số liệu, không đưa nhận định không có trong dữ liệu |
| **AI intervention point** | Sau khi số liệu đã vào template, trước bước PM viết narrative |
| **Mức chọn** | Workflow |
| **Rủi ro & người kiểm tra** | Bịa nhận định, sai số, bỏ sót blocker → PM kiểm từng con số và đối chiếu Slack trước khi gửi |

| Trường | v0 | v1 | Vì sao đổi |
|---|---|---|---|
| Actor | Junior PM phụ trách báo cáo tuần cho leadership | Thêm: ở team mà leadership đọc phần narrative | Phỏng vấn: có team chỉ cần số, với họ No AI là đủ |
| Success Metric | Chỉ đo thời gian | Thêm tỉ lệ viết lại và số câu hỏi lại | Phản biện: nhanh hơn nhưng tệ hơn thì không đạt |

**Tiêu chí đánh giá bản nháp:**

| # | Tiêu chí | Đạt khi | Không đạt khi |
|---:|---|---|---|
| 1 | Đúng số liệu | Mọi con số khớp Jira/Sheets | Có số AI tự tính hoặc làm tròn sai |
| 2 | Không bỏ sót blocker | Mọi blocker có trong input đều được nêu | Thiếu blocker có trong thread Slack |
| 3 | Không bịa | Mọi nhận định truy được về input | Có nhận định không có nguồn |
| 4 | Đọc được trong 2 phút | Dưới 250 từ, đủ 3 phần | Dài, lan man hoặc thiếu phần |

## 8. Quyết định (CP6)

| Rủi ro | Mức độ rủi ro (Thấp = an toàn) | Lý do / bằng chứng |
|---|---|---|
| **Value** | Trung bình | 2/3 phỏng vấn và 4/6 poll xác nhận pain; nhưng giả định "leadership đọc narrative" mới chỉ có 1 nguồn |
| **Usability** | Thấp | PM chỉ cần sửa văn bản, không phải học công cụ mới |
| **Feasibility** | Thấp | Rovo, tóm tắt Slack, n8n đều có sẵn; dữ liệu đã có |
| **Viability** | Trung bình | Chưa biết chính sách công ty về đưa dữ liệu nội bộ vào AI; Rovo có thể tốn thêm phí |

**Quyết định: Go, phạm vi nhỏ.**

**Lý do:** không có rủi ro mức Cao. Hai rủi ro Trung bình kiểm được ngay trong pilot.

**Pilot nhỏ nhất (2 tuần):**

- Không xây gì. PM dán số liệu + tóm tắt Slack vào một prompt chuẩn (hoặc dùng Rovo nếu công ty đã có).
- PM ghi giờ, ghi phần nháp phải sửa, chấm nháp theo 4 tiêu chí đánh giá.
- Trước pilot: hỏi EM về chính sách dữ liệu (giả định #5), hỏi CEO có đọc narrative không (giả định #3).

**Ngưỡng dừng:**

- Nếu 2 tuần liên tiếp PM phải viết lại trên 70% bản nháp → quay về template + dashboard.
- Nếu có 1 lần nháp sai số liệu mà PM không phát hiện trước khi gửi → dừng pilot, xem lại bước kiểm.
- Nếu EM không cho phép đưa dữ liệu vào AI → No-Go, dùng phương án template.

## 9. Hạn chế và hướng tiếp theo

- Baseline mới có 2 tuần của 1 người. Cần thêm dữ liệu từ 2 PM còn lại.
- "Tìm quyết định cũ trong Slack" là candidate tiềm năng cho vòng sau.

---

# Phần cá nhân — reflection (của Minh)

## 4. Tôi đã tham gia phần nào

| Hoạt động | Tôi đã làm gì? | Kết quả |
|---|---|---|
| Pitch Problem Card | Pitch "Báo cáo tuần" | Vào shortlist và được chọn |
| Phản biện bài bạn khác | Hỏi Lan: "Bạn có quyền đọc toàn bộ Slack của công ty không?" | Nhóm thấy bài "Tìm quyết định cũ" có rủi ro Feasibility cao |
| Nhận phản biện | Huy hỏi: "Template thôi có đủ không?" | Tôi thêm phương án No AI và đưa vào phỏng vấn để kiểm |
| Kiểm chứng / research | Phỏng vấn 1 PO; tìm Rovo và template n8n | Nhóm đổi từ "tự xây" sang "dùng công cụ có sẵn" |
| Quy trình nhóm | Vẽ quy trình hiện tại và tương lai | Nhóm dùng làm bản cuối |

## 5. Dùng AI

| Checkpoint | Dùng AI để làm gì? | Hữu ích ở đâu? | Sai/hời hợt ở đâu? | Tôi sửa gì |
|---|---|---|---|---|
| CP1 Scan | Gợi ý thêm problem theo vai trò PM | Nhớ ra #9, #10 | Một ý quá rộng ("trợ lý quản lý dự án") | Bỏ ý không có quy trình thật |
| CP2 Card | Đóng vai PM hoài nghi | Chỉ ra baseline chỉ dựa trí nhớ | Gợi ý agent tự gửi báo cáo | Giữ boundary PM duyệt |
| CP4 Research | Tìm công cụ tương tự | Gợi ý Rovo, n8n, Slack AI | Đưa 1 link Google Help đã đổi địa chỉ; nói Slack AI có sẵn ở mọi gói | Tự mở từng link; kiểm trang giá Slack: gói Pro chỉ có tóm tắt cơ bản |
| CP5 Quy trình | Chuyển mô tả sang Mermaid | Nhanh | Gộp "viết narrative" và "review" thành 1 bước | Tách lại vì bottleneck nằm ở narrative |

## 6. Reflection (trích)

> Lúc đầu tôi chắc chắn mình sẽ "xây một công cụ AI viết báo cáo". Đến khi research, tôi thấy Jira đã có Rovo, có cả template n8n làm gần đúng việc đó. Phần đáng làm hóa ra không phải xây công cụ, mà là xác định rõ bước nào cần người kiểm và đo thế nào là nháp "đạt". Tôi cũng bất ngờ khi một người phỏng vấn nói CEO của họ chỉ xem số: nếu không hỏi, nhóm đã viết Problem Statement cho mọi PM, trong khi với team đó thì template là đủ.
>
> Nếu làm lại, tôi sẽ hỏi CEO thật của công ty trước khi chốt metric, vì giả định "leadership đọc narrative" là giả định quan trọng nhất mà nhóm vẫn chưa kiểm chứng xong.
