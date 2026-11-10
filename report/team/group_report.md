# Báo cáo nhóm — Day 02 Discovery & Problem Framing

> Bản chung của nhóm, viết trên repo do nhóm trưởng fork. Không copy file này sang repo cá nhân.
> Template chi tiết và prompt mẫu: [docs/01-worksheet.md](../../docs/01-worksheet.md). Bài mẫu: [docs/02-deliverable-example.md](../../docs/02-deliverable-example.md).

## 1. Thông tin nhóm

- Tên nhóm:G2
- Thành viên: xem `TEAM.md`
- Candidate problem được chọn (1 câu):Ưu tiên cảnh báo giao dịch đáng ngờ, giúp Fraud Analyst xác định các giao dịch rủi ro cao cần kiểm tra trước.
- Quyết định cuối: Not Yet

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

| # | Giả định | Loại | Quan trọng (1–5) | Đã có bằng chứng (1–5) | Kiểm chứng trước? |
|---:|---|---|---:|---:|---|
| 1 | Fraud Analyst phải xử lý nhiều cảnh báo giao dịch mỗi ngày, việc kiểm tra từng cảnh báo tốn khá nhiều thời gian. | Value | 5 | 1 | Có |
| 2 | Khi có nhiều cảnh báo cùng lúc, việc xác định giao dịch nào cần kiểm tra trước vẫn còn khó khăn. | Value | 5 | 1 | Có |
| 3 | Cách ưu tiên cảnh báo hiện tại có thể khiến một số giao dịch rủi ro cao bị xử lý chậm. | Value | 5 | 1 | Có |
| 4 | Fraud Analyst có thể sử dụng danh sách cảnh báo được xếp theo mức rủi ro, kèm thông tin giải thích lý do ưu tiên. | Usability | 4 | 1 | Không |
| 5 | Dữ liệu giao dịch có đủ thông tin để thử nghiệm phân loại hoặc xếp hạng mức độ rủi ro bằng rule-based và ML. | Feasibility | 5 | 1 | Có |
| 6 | Nếu giảm được thời gian kiểm tra mà vẫn hạn chế bỏ sót gian lận, giải pháp có thể mang lại giá trị cho bộ phận Fraud Operations. | Viability | 4 | 1 | Không |

**Giả định nhóm ưu tiên kiểm chứng:** #1, #2 và #3.

Nhóm chọn ba giả định này vì chúng liên quan trực tiếp đến vấn đề cần giải quyết. Trước khi xây dựng giải pháp, nhóm cần làm rõ liệu khối lượng cảnh báo, cách xác định thứ tự ưu tiên và nguy cơ xử lý chậm có thực sự là những khó khăn đáng quan tâm hay không.

### 3.2. Kiểm chứng

**Cách kiểm chứng:** Phỏng vấn trực tiếp.

**Mục tiêu:** Tìm hiểu cách Fraud Analyst xử lý cảnh báo giao dịch, những khó khăn khi xác định thứ tự ưu tiên và các yếu tố có thể khiến giao dịch rủi ro cao bị xử lý chậm.



#### Interview Snapshot #1

| Trường | Nội dung |
|---|---|
| Người được hỏi | Nhân viên kiểm tra giao dịch |
| Câu nói đáng nhớ nhất | “Nếu có nhiều cảnh báo cùng lúc, tôi thường xem những giao dịch có dấu hiệu bất thường rõ nhất trước, chứ không kiểm tra lần lượt từ trên xuống.”  |
| Lần gần nhất gặp vấn đề này: chuyện gì đã xảy ra? | Trong một ngày có lượng giao dịch tăng cao, nhiều cảnh báo phát sinh trong cùng khoảng thời gian. Danh sách gồm cả những giao dịch thông thường và những trường hợp có dấu hiệu đáng ngờ, khiến nhân viên phải xem qua thông tin từng cảnh báo để xác định trường hợp cần ưu tiên. |
| Hiện đang xử lý bằng cách nào (workaround)? | Dựa vào giá trị giao dịch, tần suất phát sinh và lịch sử hoạt động của tài khoản để lựa chọn những trường hợp cần kiểm tra trước. |
| Mất bao lâu, bao lần? | Uớc tính trung bình 5 phút/cảnh báo . |
| Insight / opportunity rút ra | Việc xác định thứ tự ưu tiên có thể làm tăng thời gian rà soát ban đầu khi nhiều cảnh báo xuất hiện cùng lúc. Một danh sách được sắp xếp theo mức độ rủi ro có thể hỗ trợ bước này. |

#### Interview Snapshot #2

| Trường | Nội dung |
|---|---|
| Người được hỏi |  Nhân viên giám sát giao dịch |
| Câu nói đáng nhớ nhất | “Có những giao dịch nhìn qua khá bình thường, nhưng khi xem lịch sử thì mới thấy có điểm đáng nghi.”  |
| Lần gần nhất gặp vấn đề này: chuyện gì đã xảy ra? | Một tài khoản phát sinh nhiều giao dịch chuyển tiền liên tiếp với giá trị không quá lớn. Nếu chỉ xét từng giao dịch riêng lẻ thì chưa có dấu hiệu rõ ràng. Tuy nhiên, khi đối chiếu lịch sử, nhân viên nhận thấy tần suất giao dịch tăng bất thường và cần kiểm tra kỹ hơn. |
| Hiện đang xử lý bằng cách nào (workaround)? | Kiểm tra lịch sử giao dịch, đối chiếu với hoạt động trước đó và xem xét thêm các dấu hiệu liên quan trước khi đưa ra đánh giá. |
| Mất bao lâu, bao lần? | Ước tính 5p cho một lịch sử giao dịch, nhưng số lượng tài khoản rất nhiều |
| Insight / opportunity rút ra | Mức độ rủi ro không thể đánh giá chỉ dựa trên số tiền giao dịch. Hệ thống hỗ trợ nên cung cấp thêm thông tin về tần suất và lịch sử hoạt động để người kiểm tra có đủ cơ sở đánh giá. |

#### Interview Snapshot #3

| Trường | Nội dung |
|---|---|
| Người được hỏi |  Nhân viên kiểm soát rủi ro |
| Câu nói đáng nhớ nhất | “Nên lọc những giao dịch có dấu hiệu bất thường trước. Nếu cảnh báo nào cũng kiểm tra thủ công thì sẽ mất khá nhiều thời gian.”  |
| Lần gần nhất gặp vấn đề này: chuyện gì đã xảy ra? | Khi rà soát một danh sách cảnh báo, nhân viên gặp nhiều giao dịch có đặc điểm tương tự nhau. Thay vì kiểm tra lần lượt, nhân viên phân nhóm theo giá trị và tần suất giao dịch để xác định các trường hợp cần chú ý trước. Một số giao dịch vẫn phải đối chiếu thêm lịch sử mới có thể đánh giá. |
| Hiện đang xử lý bằng cách nào (workaround)? | Sử dụng các dấu hiệu như giá trị giao dịch lớn, tần suất cao hoặc hoạt động khác thường để phân nhóm và ưu tiên kiểm tra. |
| Mất bao lâu, bao lần? | Ước tính mất 1 đến 2 tiếng để rà soát danh sách cảnh báo mỗi ngày |
| Insight / opportunity rút ra | Việc sàng lọc bằng các quy tắc đơn giản có thể hỗ trợ bước kiểm tra ban đầu. Nhóm nên thử nghiệm rule-based trước khi đánh giá liệu ML có mang lại hiệu quả tốt hơn hay không. |

#### Tổng hợp

| Nguồn | Số người / số mẫu | Tín hiệu xác nhận | Tín hiệu phản bác |
|---|---:|---|---|
| Phỏng vấn trực tiếp | 1 người| Khi nhiều cảnh báo xuất hiện cùng lúc, việc xác định thứ tự xử lý có thể mất thêm thời gian. | Nhân viên vẫn có thể tự ưu tiên dựa trên các dấu hiệu bất thường. |
| Phỏng vấn trực tiếp | 1 người| Một số giao dịch cần kiểm tra thêm lịch sử và tần suất phát sinh để đánh giá rủi ro. | Không phải giao dịch nào cũng cần đối chiếu nhiều bước. |
| Phỏng vấn trực tiếp | 1 người | Phân nhóm cảnh báo có thể giúp tập trung vào các trường hợp đáng chú ý. | Rule-based có thể giải quyết một phần bài toán, chưa chắc cần áp dụng ML. |

**Nhóm đã sửa problem thế nào sau kiểm chứng:**

**Problem ban đầu:**

Khi có nhiều cảnh báo giao dịch đáng ngờ, Fraud Analyst muốn ưu tiên giao dịch rủi ro cao để giảm thời gian kiểm tra và tránh bỏ sót gian lận.

**Nhận định sau khi phân tích các tình huống:**

Nhóm xác định hai khía cạnh cần tập trung là việc lựa chọn thứ tự ưu tiên và lượng thông tin cần đối chiếu trước khi đánh giá một giao dịch. Bên cạnh đó, không phải mọi cảnh báo đều cần được kiểm tra thủ công theo cùng một cách. Việc sử dụng các quy tắc sàng lọc có thể giúp giảm khối lượng rà soát ban đầu.

**Problem sau điều chỉnh (đề xuất):**

Khi phải xử lý nhiều cảnh báo giao dịch cùng lúc, Fraud Analyst cần xác định những giao dịch có mức độ rủi ro cao và có đủ thông tin để ưu tiên kiểm tra, nhằm giảm thời gian rà soát và hạn chế xử lý chậm các trường hợp đáng ngờ.

### 3.3. Research giải pháp đã có

Nhóm tìm hiểu các tài liệu về giám sát giao dịch bất thường nhằm xác định những phương pháp đang được sử dụng và lựa chọn hướng triển khai phù hợp cho bài toán.

| Nguồn | Nội dung tìm hiểu | Liên hệ với bài toán của nhóm |
|---|---|---|
| Basel Committee on Banking Supervision – Anti-money laundering and counter-terrorist financing | Đề cập đến việc quản lý và giám sát rủi ro trong hoạt động ngân hàng, bao gồm việc sử dụng thông tin khách hàng và giao dịch để nhận diện hoạt động bất thường. | Việc đánh giá rủi ro nên xem xét nhiều yếu tố, không chỉ dựa vào giá trị giao dịch. |
| Wolfsberg Group (2024) – Effective Monitoring for Suspicious Activity, Part I | Nhấn mạnh cách tiếp cận giám sát dựa trên rủi ro và hiệu quả phát hiện hoạt động đáng ngờ, thay vì chỉ tập trung vào số lượng cảnh báo. | Củng cố hướng nghiên cứu về ưu tiên cảnh báo có rủi ro cao. |
| Wolfsberg Group – Effective Monitoring for Suspicious Activity, Part II | Thảo luận về việc ứng dụng công nghệ và các phương pháp phân tích nâng cao trong giám sát hoạt động đáng ngờ. | Nhóm có thể so sánh rule-based và ML để đánh giá hiệu quả xếp hạng cảnh báo. |

**Nguồn tham khảo:**

1. Basel Committee on Banking Supervision: https://www.bis.org/committees/bcbs/basel-consolidated-guidelines/module/afs/10
2. Wolfsberg Group – Part I: https://wolfsberg-group.org/resources/general/168/
3. Wolfsberg Group – Part II: https://wolfsberg-group.org/resources/195/202

**Kết luận research:**

Qua các tài liệu, nhóm nhận thấy cách tiếp cận dựa trên mức độ rủi ro là một hướng phù hợp để nghiên cứu bài toán giám sát giao dịch. Tuy nhiên, các nguồn trên chủ yếu liên quan đến phòng chống tội phạm tài chính và giám sát hoạt động đáng ngờ, không trực tiếp xác nhận khối lượng công việc của Fraud Analyst trong phạm vi bài toán nhóm.

Vì vậy, nhóm chọn hướng thử nghiệm xếp hạng cảnh báo giao dịch theo mức độ rủi ro, kết hợp thông tin giải thích để hỗ trợ người kiểm tra.

Trước mắt, nhóm dự kiến xây dựng phương pháp rule-based làm baseline, sau đó thử nghiệm ML và so sánh dựa trên khả năng phát hiện giao dịch rủi ro cao, tỷ lệ bỏ sót và thời gian xử lý.

Các số liệu 500 cảnh báo/ngày và 5 phút/cảnh báo từ CP3 chỉ được sử dụng làm giả định ban đầu, không xem là kết quả nghiên cứu đã được xác nhận.
---

## 4. Quy trình trước/sau (CP5)

### 4.1. Quy trình hiện tại

**Sơ đồ:**

```text
[Hệ thống giám sát giao dịch]
                |
                v
[1. Tạo cảnh báo giao dịch bất thường]
       ≤5 giây/cảnh báo (ước tính)
                |
                v
[2. Fraud Analyst tiếp nhận cảnh báo]
          20 giây/cảnh báo
                |
                v
[3. Kiểm tra thông tin và lịch sử]
         180 giây/cảnh báo
         <<< BOTTLENECK >>>
                |
                v
[4. Đánh giá rủi ro, xác định ưu tiên]
          60 giây/cảnh báo
         <<< BOTTLENECK >>>
                |
                v
[5. Quyết định xử lý hoặc chuyển cấp]
          40 giây/cảnh báo

Tổng thời gian thao tác thủ công:
20 + 180 + 60 + 40 = 300 giây/cảnh báo
```

| Bước | Actor | Input | Output | Thời gian / tần suất | Ghi chú |
|---:|---|---|---|---|---|
| 1 | Hệ thống giám sát | Dữ liệu giao dịch | Cảnh báo bất thường | ≤5 giây/cảnh báo (ước tính), phát sinh liên tục | Tạo cảnh báo dựa trên quy tắc giám sát hiện có. |
| 2 | Fraud Analyst | Danh sách cảnh báo | Cảnh báo được tiếp nhận | 20 giây/cảnh báo (giả định) | Mở và xem thông tin ban đầu. |
| 3 | Fraud Analyst | Thông tin giao dịch, lịch sử tài khoản | Thông tin phục vụ đánh giá | 180 giây/cảnh báo (giả định) | Đối chiếu giá trị, tần suất và lịch sử hoạt động. |
| 4 | Fraud Analyst | Thông tin đã kiểm tra | Đánh giá rủi ro, thứ tự ưu tiên | 60 giây/cảnh báo (giả định) | Xác định trường hợp cần xử lý trước. |
| 5 | Fraud Analyst | Kết quả đánh giá | Quyết định xử lý hoặc chuyển cấp | 40 giây/cảnh báo (giả định) | Các trường hợp phức tạp có thể cần xác minh thêm. |

**Bottleneck chính:**

Bước 3 và bước 4 chiếm khoảng 240/300 giây, tương đương 80% thời gian thao tác thủ công theo mô hình ước tính. Fraud Analyst phải đối chiếu nhiều thông tin và tự xác định thứ tự ưu tiên cho các cảnh báo.

Khi lượng cảnh báo tăng, quá trình rà soát ban đầu có thể kéo dài, khiến những giao dịch có rủi ro cao không được kiểm tra kịp thời.

**Cơ sở thời gian:** Nhóm sử dụng giả định từ CP3 là 5 phút/cảnh báo và phân bổ cho từng bước để mô tả quy trình. Đây chưa phải số liệu đo thực tế.

### 4.2. Quy trình tương lai

**Sơ đồ:**

```text
[Hệ thống giám sát giao dịch]
                |
                v
[1. Tạo cảnh báo giao dịch bất thường]
       ≤5 giây/cảnh báo (ước tính)
                |
                v
[2. RULE: Kiểm tra dữ liệu và
    áp dụng quy tắc rủi ro]
          ≤2 giây/cảnh báo
                |
                v
[3. AI: Chấm điểm và xếp hạng]
          ≤7 giây/cảnh báo
                |
                v
[Kiểm tra kết quả AI có hợp lệ?]
           /          \
         Có           Không
          |              |
          v              v
[4. Hiển thị danh    [FALLBACK:
 sách ưu tiên và      Xếp hạng bằng
 lý do: ≤1 giây]      rule-based]
          |              |
          +------+-------+
                 |
                 v
[5. CON NGƯỜI: Fraud Analyst kiểm tra]
      120 giây/cảnh báo (mục tiêu)
                 |
                 v
[6. Quyết định xử lý hoặc chuyển cấp]
       40 giây/cảnh báo (mục tiêu)

Sàng lọc tự động: ≤10 giây/cảnh báo
Kiểm tra và quyết định: 160 giây/cảnh báo
Tổng mục tiêu sau khi tạo cảnh báo:
≤170 giây/cảnh báo
```

| Bước | Actor | Input | Output | Thời gian mục tiêu | Ghi chú |
|---:|---|---|---|---|---|
| 1 | Hệ thống giám sát | Dữ liệu giao dịch | Danh sách cảnh báo | ≤5 giây/cảnh báo (ước tính) | Giữ nguyên bước phát hiện ban đầu. |
| 2 | Rule | Cảnh báo và dữ liệu liên quan | Dữ liệu hợp lệ, cờ rủi ro | ≤2 giây/cảnh báo | Kiểm tra dữ liệu và áp dụng quy tắc bắt buộc. |
| 3 | AI | Dữ liệu và đặc trưng giao dịch | Điểm rủi ro, thứ tự ưu tiên | ≤7 giây/cảnh báo | Chấm điểm và đề xuất thứ tự ưu tiên. |
| 4 | Hệ thống | Kết quả Rule và AI | Danh sách ưu tiên kèm lý do | ≤1 giây/cảnh báo | Hiển thị thông tin hỗ trợ người kiểm tra. |
| 5 | Fraud Analyst | Danh sách ưu tiên, thông tin giao dịch | Kết quả kiểm tra | 120 giây/cảnh báo (mục tiêu giả định) | Kiểm tra chuyên sâu các trường hợp đáng ngờ. |
| 6 | Fraud Analyst | Kết quả kiểm tra | Quyết định xử lý hoặc chuyển cấp | 40 giây/cảnh báo (mục tiêu giả định) | Con người chịu trách nhiệm cuối cùng. |

**Phân chia trách nhiệm:**

- **Rule:** Kiểm tra dữ liệu đầu vào, phát hiện thông tin thiếu và áp dụng các quy tắc rủi ro bắt buộc. Cảnh báo vi phạm quy tắc quan trọng vẫn được ưu tiên ngay cả khi AI đánh giá thấp.
- **AI:** Phân tích đặc trưng giao dịch, dự đoán điểm rủi ro và đề xuất thứ tự ưu tiên. Hiển thị những yếu tố chính ảnh hưởng đến kết quả nếu mô hình hỗ trợ giải thích.
- **Con người:** Fraud Analyst kiểm tra thông tin, đánh giá các trường hợp đáng ngờ và quyết định xử lý hoặc chuyển cấp.

**Boundary (giới hạn của AI):**

AI chỉ hỗ trợ sàng lọc và xếp hạng cảnh báo. AI không được tự động khóa tài khoản, từ chối giao dịch, xóa cảnh báo, đóng hồ sơ hoặc kết luận giao dịch là gian lận.

Fraud Analyst có quyền xem xét lại và thay đổi mức ưu tiên do AI đề xuất. Những trường hợp rủi ro cao, dữ liệu thiếu hoặc kết quả không rõ ràng cần được con người kiểm tra.

**Phương án quay về (Fallback):**

Khi AI gặp lỗi, không phản hồi trong thời gian cho phép, thiếu dữ liệu hoặc trả về kết quả không hợp lệ, hệ thống chuyển sang xếp hạng bằng rule-based.

Toàn bộ cảnh báo được giữ lại trong danh sách. Fraud Analyst tiếp tục kiểm tra thủ công theo thứ tự ưu tiên của rule-based. Hệ thống ghi nhận lỗi để phục vụ kiểm tra và khôi phục AI sau khi sự cố được xử lý.

Mốc ≤10 giây là mục tiêu của luồng sàng lọc bình thường. Độ trễ của nhánh fallback cần được đo riêng.

**Lợi ích kỳ vọng:**

Quy trình mới tự động hóa việc sàng lọc và xếp hạng cảnh báo trong tối đa 10 giây/cảnh báo, giúp Fraud Analyst tiếp cận những giao dịch cần chú ý sớm hơn.

Nhóm đặt mục tiêu giảm thời gian xử lý từ 300 giây xuống tối đa 170 giây/cảnh báo. Tuy nhiên, mức giảm này chỉ là kịch bản kỳ vọng, chưa phải hiệu quả đã được chứng minh.

### 4.3. Before / after

| Chỉ số | Trước | Sau (kỳ vọng) | Ghi chú |
|---|---|---|---|
| Số bước | 5 | 6 | Bổ sung Rule và AI để hỗ trợ tự động hóa. |
| Tổng thời gian xử lý sau khi tạo cảnh báo | 300 giây/cảnh báo (giả định) | ≤170 giây/cảnh báo (mục tiêu giả định) | Giảm khoảng 43,3% theo kịch bản; cần đo thực tế để xác minh. |
| Thời gian sàng lọc và đánh giá ban đầu | 260 giây/cảnh báo (bước 2–4, giả định) | ≤10 giây/cảnh báo cho Rule + AI + hiển thị | Hai phạm vi chưa hoàn toàn tương đương vì bước kiểm tra của con người vẫn tồn tại; không dùng trực tiếp để kết luận mức tiết kiệm. |
| Số bước thủ công | 4 | 2 | Tự động hóa một phần công việc sàng lọc, con người tiếp tục kiểm tra và quyết định. |
| Bottleneck chính | Đối chiếu thông tin và tự xác định thứ tự ưu tiên | Kiểm tra chuyên sâu những cảnh báo phức tạp | Giảm thao tác phân loại ban đầu. |
| Rủi ro mới phát sinh | Xử lý chậm, ưu tiên không nhất quán | AI xếp hạng sai, dữ liệu thiếu hoặc hệ thống lỗi | Duy trì rule-based fallback, HITL và theo dõi chất lượng xếp hạng. |

**Kết luận before/after:**

Quy trình tương lai chuyển công việc sàng lọc và xếp hạng ban đầu từ Fraud Analyst sang Rule và AI, đồng thời giữ quyền quyết định cuối cùng cho con người.

Theo kịch bản giả định, thời gian xử lý giảm từ 300 giây xuống 170 giây/cảnh báo, tương đương khoảng 43,3%. Nhóm cần đo thời gian thực tế trên cùng tập cảnh báo, với cùng điểm bắt đầu và kết thúc, để xác minh mức cải thiện này.

---

## 5. Problem Statement v0 (CP5)

| Trường | Nội dung |
|---|---|
| **Actor** | Fraud Analyst / Fraud Operations Team – nhân sự phụ trách rà soát và xử lý cảnh báo giao dịch đáng ngờ. |
| **Quy trình** | Tiếp nhận cảnh báo, kiểm tra thông tin và lịch sử giao dịch, đánh giá rủi ro, xác định thứ tự ưu tiên và quyết định xử lý hoặc chuyển cấp. |
| **Bottleneck** | Fraud Analyst phải tự đối chiếu thông tin và xác định thứ tự ưu tiên khi có nhiều cảnh báo cùng lúc. Theo phân bổ thời gian giả định, hai bước này chiếm khoảng 80% thời gian thao tác thủ công. |
| **Impact** | Tăng khối lượng rà soát thủ công và nguy cơ xử lý chậm cảnh báo quan trọng. Với giả định 500 cảnh báo/ngày và 5 phút/cảnh báo từ CP3, khối lượng kiểm tra tương đương khoảng 41,7 giờ công/ngày. Đây là ước tính, chưa được xác minh. |
| **Success Metric** (baseline → target, cách đo) | **Thời gian xử lý toàn quy trình:** baseline 300 giây/cảnh báo (giả định), target chưa xác định; đo từ khi Fraud Analyst tiếp nhận cảnh báo đến khi quyết định hoặc chuyển cấp. **Thời gian sàng lọc tự động:** chưa có baseline, target ≤10 giây/cảnh báo; đo từ khi cảnh báo đi vào bộ Rule + AI đến khi hiển thị danh sách ưu tiên. **Chất lượng ưu tiên:** đo Recall@K và Precision@K của rule-based baseline, kỳ vọng AI cải thiện trên cùng tập kiểm thử có nhãn. **An toàn:** recall phát hiện gian lận không thấp hơn baseline. |
| **Boundary** (AI không được làm gì; khi nào cần con người kiểm tra — HITL) | AI chỉ chấm điểm, xếp hạng và hỗ trợ giải thích; không tự khóa tài khoản, từ chối giao dịch, xóa cảnh báo hoặc kết luận gian lận. Fraud Analyst chịu trách nhiệm quyết định cuối cùng. Khi AI lỗi, thiếu dữ liệu hoặc kết quả không hợp lệ, hệ thống chuyển về rule-based và kiểm tra thủ công. |

**Phản biện nhận được (từ AI) và nhóm có đồng ý không:**

- **Phản biện 1:** AI có thể xếp hạng sai, khiến giao dịch gian lận bị đưa xuống nhóm ưu tiên thấp.
  - **Nhóm đồng ý.** Hệ thống không tự động loại bỏ cảnh báo có điểm thấp, duy trì các quy tắc rủi ro bắt buộc và sử dụng Recall@K để đánh giá khả năng ưu tiên đúng.

- **Phản biện 2:** Rule-based có thể đã đáp ứng nhu cầu sàng lọc, chưa chắc cần triển khai ML.
  - **Nhóm đồng ý.** Nhóm sử dụng rule-based làm baseline và chỉ lựa chọn ML nếu kết quả thử nghiệm cho thấy cải thiện có thể đo lường.

- **Phản biện 3:** Mục tiêu 10 giây/cảnh báo không phản ánh toàn bộ thời gian xử lý giao dịch.
  - **Nhóm đồng ý.** Mốc 10 giây chỉ áp dụng cho khâu sàng lọc tự động. Thời gian kiểm tra và quyết định của Fraud Analyst được đo riêng.

- **Phản biện 4:** Các số liệu về khối lượng cảnh báo và thời gian xử lý hiện tại chưa được xác minh.
  - **Nhóm đồng ý.** Nhóm sử dụng các số liệu từ CP3 làm giả định ban đầu và sẽ cập nhật sau khi có dữ liệu thử nghiệm.

---
## 6. Mức can thiệp AI (CP6)

### 6.1. Ma trận độ mơ hồ × độ phức tạp

| Tiêu chí | Mức đánh giá | Lý do |
|---|---|---|
| Độ mơ hồ (Ambiguity) | Cao | Một giao dịch bất thường chưa chắc là gian lận. Mức độ rủi ro phụ thuộc vào bối cảnh, lịch sử và hành vi giao dịch, nên khó xác định chỉ bằng một quy tắc cố định. |
| Độ phức tạp (Complexity) | Cao | Việc ưu tiên cảnh báo có thể cần kết hợp nhiều đặc trưng như số tiền, thời điểm, tần suất, lịch sử và các tín hiệu rủi ro khác. Các yếu tố này có thể tương tác với nhau. |

**Vị trí trong ma trận: Độ mơ hồ cao × Độ phức tạp cao.**

Bài toán có nhiều yếu tố cần xem xét và không phải lúc nào cũng có một quy tắc đơn giản để xác định thứ tự ưu tiên. Tuy nhiên, quy trình xử lý vẫn có thể được thiết kế theo các bước cố định, không nhất thiết cần một AI Agent tự chủ.

Vì vậy, nhóm xem xét Workflow kết hợp Rule, ML và sự kiểm tra của Fraud Analyst.

### 6.2. So sánh bốn mức can thiệp

| Mức | Cách áp dụng cho bài toán | Ưu điểm | Hạn chế | Quyết định |
|---|---|---|---|---|
| **No AI** | Fraud Analyst tự xem xét và ưu tiên cảnh báo. | Không cần xây dựng mô hình, con người kiểm soát toàn bộ. | Tốn thời gian rà soát và khó duy trì thứ tự ưu tiên nhất quán khi số lượng cảnh báo tăng. | Không chọn làm hướng cải tiến chính. |
| **Rule** | Sử dụng các điều kiện cố định về số tiền, tần suất hoặc dấu hiệu bất thường để xếp hạng. | Đơn giản, dễ giải thích, dễ triển khai và kiểm thử. | Có thể khó biểu diễn các mẫu rủi ro phức tạp hoặc thay đổi theo thời gian. | Dùng làm baseline và fallback. |
| **Workflow** | Rule kiểm tra điều kiện bắt buộc, ML dự đoán điểm rủi ro và xếp hạng, Fraud Analyst kiểm tra và quyết định. | Kết hợp tính kiểm soát của Rule với khả năng học từ dữ liệu của ML; có thể đo lường và kiểm tra từng bước. | Phụ thuộc chất lượng dữ liệu và cần theo dõi sai lệch của mô hình. | **Chọn để thử nghiệm.** |
| **Agent** | AI tự lập kế hoạch, truy xuất nhiều nguồn thông tin, lựa chọn công cụ và thực hiện các bước xử lý linh hoạt. | Phù hợp khi quy trình cần nhiều quyết định và hành động thay đổi theo tình huống. | Tăng độ phức tạp, khó kiểm soát và kiểm thử hơn; không cần thiết cho nhiệm vụ chấm điểm và xếp hạng cố định. | Không chọn. |

**Vì sao không chỉ dùng Rule?**

Rule-based có thể xử lý các dấu hiệu rõ ràng, nhưng có khả năng bỏ qua những mẫu rủi ro hình thành từ sự kết hợp của nhiều đặc trưng. Nhóm muốn thử nghiệm ML để kiểm tra liệu khả năng xếp hạng có cải thiện so với Rule hay không.

Tuy nhiên, nhóm chưa có bằng chứng ML tốt hơn Rule. Vì vậy, Rule vẫn là baseline và nhóm chỉ tiếp tục hướng ML khi đạt các tiêu chí đánh giá ở Mục 7.

**Vì sao không chọn Agent?**

Bài toán hiện tại chỉ yêu cầu chấm điểm và đề xuất thứ tự ưu tiên trong một quy trình đã xác định. Hệ thống không cần AI tự lập kế hoạch hoặc tự thực hiện hành động trên tài khoản giao dịch. Workflow đủ để thử nghiệm mục tiêu này, đồng thời dễ kiểm soát hơn Agent.

**Kết luận:** Nhóm lựa chọn **Workflow (Rule + ML + Human-in-the-Loop)** làm hướng thử nghiệm, chưa quyết định triển khai thực tế.

### 6.3. AI Canvas

| Thành phần | Nội dung áp dụng |
|---|---|
| **Prediction** | Dự đoán điểm rủi ro cho mỗi cảnh báo giao dịch và đề xuất thứ tự ưu tiên kiểm tra. |
| **Judgment** | Fraud Analyst đánh giá mức độ đáng ngờ dựa trên điểm rủi ro, thông tin giao dịch, lịch sử và các quy tắc nghiệp vụ. |
| **Action** | Hệ thống hiển thị danh sách cảnh báo theo thứ tự ưu tiên; Fraud Analyst quyết định kiểm tra, xử lý hoặc chuyển cấp. |
| **Outcome** | Cải thiện Recall@K và Precision@K so với rule-based baseline, giảm thời gian xử lý và hạn chế bỏ sót các trường hợp gian lận trong nhóm cảnh báo được ưu tiên. |
| **Input** | Dữ liệu giao dịch như số tiền, thời điểm, tần suất, lịch sử hoạt động, đặc trưng hành vi và các cờ rủi ro từ Rule. Việc sử dụng từng loại dữ liệu phụ thuộc vào dataset thực tế. |
| **Feedback** | Kết quả kiểm tra của Fraud Analyst, nhãn gian lận đã được xác minh, các trường hợp xếp hạng sai và phản hồi về mức độ hữu ích của danh sách ưu tiên. |

**Dữ liệu tối thiểu cần kiểm tra trước khi triển khai:**

- Mã định danh cảnh báo/giao dịch để theo dõi và đối chiếu kết quả.
- Các đặc trưng giao dịch có sẵn tại thời điểm phát sinh cảnh báo.
- Nhãn gian lận đáng tin cậy để huấn luyện hoặc đánh giá.
- Kết quả xếp hạng của Rule để xây dựng baseline.
- Thời điểm bắt đầu và kết thúc xử lý để đo hiệu quả quy trình.

Nhóm chưa xác nhận dataset có đầy đủ các trường trên. Nếu thiếu lịch sử giao dịch, nhãn hoặc thông tin thời gian, cần điều chỉnh phạm vi thử nghiệm và không khẳng định mô hình có thể hoạt động như trong môi trường thực tế.

### 6.4. Hai câu hỏi Google PAIR

**Câu hỏi 1: AI nên hỗ trợ con người (augment) hay tự động thay thế (automate)?**

Nhóm lựa chọn **augment** đối với quyết định nghiệp vụ và **automate** đối với bước tính điểm, sắp xếp cảnh báo.

AI hỗ trợ Fraud Analyst xác định các cảnh báo cần chú ý trước, nhưng không thay thế việc kiểm tra và đưa ra quyết định cuối cùng. Fraud Analyst có thể xem thông tin hỗ trợ, điều chỉnh mức ưu tiên và chuyển cấp khi cần.

**Câu hỏi 2: Nếu AI dự đoán sai, lỗi nào gây hậu quả nghiêm trọng hơn?**

Trong phạm vi ưu tiên cảnh báo, nhóm đánh giá **False Negative** — giao dịch gian lận bị đánh giá rủi ro thấp hoặc không được ưu tiên — là rủi ro cần kiểm soát đặc biệt, vì có thể khiến việc kiểm tra bị chậm.

**False Positive** — giao dịch bình thường bị ưu tiên cao — cũng gây ảnh hưởng vì làm tăng khối lượng rà soát và có thể khiến Fraud Analyst mất thời gian.

Để hạn chế hai loại sai sót, nhóm đề xuất:

- Không tự động xóa hoặc đóng cảnh báo có điểm rủi ro thấp.
- Duy trì các quy tắc bắt buộc để những cảnh báo quan trọng không bị ML hạ mức ưu tiên.
- Đánh giá Recall@K và Precision@K trên cùng tập dữ liệu với rule-based baseline.
- Cho phép Fraud Analyst xem xét và điều chỉnh mức ưu tiên.
- Chuyển về rule-based khi AI lỗi, thiếu dữ liệu hoặc trả về kết quả không hợp lệ.

**Kết luận PAIR:** AI được sử dụng để hỗ trợ sàng lọc và ưu tiên, trong khi con người giữ quyền kiểm tra và quyết định cuối cùng. Hệ thống ưu tiên tính an toàn, khả năng giải thích và kiểm soát sai sót hơn mức độ tự động hóa.

## 7. Problem Statement v1 + tiêu chí đánh giá (CP6)

| Trường | Nội dung |
|---|---|
| **Actor** | Fraud Analyst / Fraud Operations Team – nhân sự phụ trách rà soát và xử lý cảnh báo giao dịch đáng ngờ. |
| **Quy trình** | Hệ thống tiếp nhận cảnh báo, Rule kiểm tra dữ liệu và áp dụng điều kiện rủi ro, ML chấm điểm và xếp hạng, Fraud Analyst kiểm tra và quyết định xử lý hoặc chuyển cấp. |
| **Bottleneck** | Việc đối chiếu thông tin và tự xác định thứ tự ưu tiên cho nhiều cảnh báo còn tốn thời gian. Theo mô hình thời gian giả định ở CP5, hai bước này chiếm khoảng 80% thời gian thao tác thủ công. |
| **Impact** | Tăng khối lượng rà soát và nguy cơ xử lý chậm các cảnh báo rủi ro cao. Với giả định 500 cảnh báo/ngày × 5 phút/cảnh báo, tổng khối lượng kiểm tra tương đương khoảng 41,7 giờ công/ngày; chưa phải số liệu thực tế. |
| **Success Metric** (baseline → target, cách đo) | **Thời gian toàn quy trình:** baseline 300 giây/cảnh báo (giả định) → target ≤170 giây/cảnh báo (mục tiêu giả định); đo từ khi cảnh báo được tiếp nhận đến khi Fraud Analyst quyết định hoặc chuyển cấp, trên cùng tập cảnh báo. **Thời gian sàng lọc:** baseline thủ công cần đo → target p95 ≤10 giây/cảnh báo cho Rule + ML + hiển thị; ghi timestamp đầu/cuối khâu tự động. **Chất lượng ưu tiên:** Recall@K của rule-based baseline → mục tiêu tăng ≥5 điểm phần trăm trên cùng tập kiểm thử. **An toàn:** recall phát hiện gian lận không thấp hơn baseline. **Fallback:** giữ lại 100% cảnh báo khi AI lỗi. |
| **Boundary** | AI chỉ chấm điểm, xếp hạng và hỗ trợ giải thích. Không tự khóa tài khoản, từ chối giao dịch, xóa cảnh báo hoặc kết luận gian lận. Fraud Analyst đưa ra quyết định cuối cùng. |
| **AI intervention point** | Sau khi hệ thống tạo cảnh báo và Rule kiểm tra dữ liệu, trước khi Fraud Analyst tiếp nhận danh sách ưu tiên. |
| **Mức chọn** | **Workflow** — Rule + ML + HITL. |
| **Rủi ro & người kiểm tra** | Rủi ro chính là AI xếp hạng sai, bỏ sót giao dịch quan trọng, dữ liệu thiếu hoặc mô hình suy giảm chất lượng. Fraud Analyst kiểm tra các cảnh báo; nhóm kỹ thuật theo dõi metric, log và kích hoạt fallback khi cần. |

**Thay đổi so với v0 và lý do:**

| Trường | v0 | v1 | Vì sao đổi |
|---|---|---|---|
| Quy trình | Mô tả Rule + AI hỗ trợ sàng lọc. | Xác định rõ Workflow gồm Rule + ML + HITL. | Làm rõ mức can thiệp AI và trách nhiệm từng thành phần. |
| Success Metric | Đặt mục tiêu sàng lọc ≤10 giây, chưa có target thời gian toàn quy trình. | Bổ sung mục tiêu ≤170 giây toàn quy trình, p95 sàng lọc ≤10 giây và Recall@K tăng ≥5 điểm phần trăm. | Đảm bảo các chỉ số có mục tiêu định lượng và phương pháp kiểm chứng rõ ràng. |
| Boundary | AI không tự xử lý giao dịch. | Giữ boundary, làm rõ quyền điều chỉnh ưu tiên của Fraud Analyst và fallback. | Hạn chế tác động khi AI dự đoán sai. |
| Kiểm soát lỗi | Chuyển sang rule-based khi AI lỗi. | Đặt mục tiêu giữ lại 100% cảnh báo khi fallback. | Có tiêu chí kiểm thử rõ ràng cho an toàn hệ thống. |
| AI intervention point | Chưa tách thành trường riêng. | Sau Rule, trước khi Fraud Analyst kiểm tra. | Xác định chính xác vị trí AI trong quy trình. |
| Rủi ro & người kiểm tra | Chưa tách thành trường riêng. | Fraud Analyst kiểm tra nghiệp vụ, nhóm kỹ thuật theo dõi mô hình. | Xác định trách nhiệm khi AI gặp lỗi. |

**Tiêu chí đánh giá đầu ra của AI:**

| # | Tiêu chí | Đạt khi | Không đạt khi |
|---:|---|---|---|
| 1 | Chất lượng ưu tiên | Recall@K tăng ít nhất 5 điểm phần trăm so với rule-based baseline trên cùng tập kiểm thử. | Recall@K không đạt mức cải thiện đề ra. |
| 2 | Hạn chế bỏ sót | Recall phát hiện gian lận không thấp hơn baseline tại ngưỡng đánh giá đã chọn. | Recall giảm, làm tăng số giao dịch gian lận bị bỏ sót. |
| 3 | Tốc độ xử lý | p95 thời gian Rule + ML + hiển thị ≤10 giây/cảnh báo. | p95 vượt 10 giây/cảnh báo. |
| 4 | Khả năng kiểm tra kết quả | 100% cảnh báo được xử lý có điểm rủi ro, thứ tự ưu tiên và thông tin hỗ trợ đánh giá có thể truy xuất. | Có cảnh báo thiếu thông tin cần thiết hoặc không thể truy vết kết quả. |
| 5 | Khả năng xử lý lỗi | Khi ML lỗi hoặc dữ liệu không hợp lệ, hệ thống chuyển về rule-based và giữ lại 100% cảnh báo. | Có cảnh báo bị mất hoặc hệ thống không thể chuyển sang phương án dự phòng. |

**Lưu ý về đánh giá:** Các mục tiêu ≤170 giây, ≤10 giây và Recall@K tăng ≥5 điểm phần trăm là ngưỡng thử nghiệm nhóm đề xuất. Kết quả thực tế cần được đo trên tập dữ liệu có nhãn và trong điều kiện thử nghiệm xác định trước. Giá trị K cần cố định theo số cảnh báo mà Fraud Analyst có thể kiểm tra trong một phiên làm việc.
---

## 8. Quyết định (CP6)

### 8.1. Bốn rủi ro

| Rủi ro | Câu hỏi | Mức độ rủi ro | Lý do / bằng chứng |
|---|---|---|---|
| **Value** | Người dùng có thật sự cần và sẽ dùng không? | **Cao** | Bài toán được xác định từ các giả định CP3–CP4 nhưng chưa được xác nhận bằng phỏng vấn Fraud Analyst thực tế. Chưa chứng minh được mức độ nghiêm trọng và nhu cầu sử dụng. |
| **Usability** | Người dùng có dùng được, có hiểu và sửa được đầu ra của AI không? | **Trung bình** | Danh sách xếp hạng và điểm rủi ro tương đối dễ trình bày. Tuy nhiên, chưa thử nghiệm giao diện với người dùng thực tế để xác nhận mức độ dễ hiểu và khả năng điều chỉnh. |
| **Feasibility** | Có đủ dữ liệu, công cụ, kỹ năng để làm không? | **Trung bình** | Có thể xây dựng rule-based và thử nghiệm ML bằng Python, scikit-learn hoặc các công cụ tương đương. Rủi ro chính là chất lượng dataset, nhãn gian lận, mất cân bằng lớp và khả năng tạo đặc trưng lịch sử. |
| **Viability** | Có hợp chi phí, pháp lý, quy định tổ chức không? Ai vận hành? | **Cao** | Dữ liệu giao dịch có tính nhạy cảm; chưa có xác nhận về quyền truy cập dữ liệu, chi phí triển khai thực tế và đơn vị chịu trách nhiệm vận hành. |

### 8.2. Kết luận

**Quyết định: Not Yet — chưa triển khai thực tế; cho phép kiểm chứng bằng prototype nhỏ.**

**Lý do:**

Bài toán có hướng giải pháp khả thi về mặt kỹ thuật và có thể xây dựng một prototype để đánh giá. Tuy nhiên, nhóm chưa có đủ bằng chứng về nhu cầu thực tế của Fraud Analyst, chất lượng dữ liệu và khả năng cải thiện so với rule-based.

Vì vậy, nhóm chưa nên kết luận ML là giải pháp cần thiết hoặc triển khai trên dữ liệu giao dịch thật. Bước tiếp theo phù hợp là kiểm chứng nhu cầu và thử nghiệm trên dữ liệu công khai hoặc dữ liệu giả lập.

**Nếu Go — pilot nhỏ nhất:**

Xây dựng một prototype offline gồm Rule + ML + bảng xếp hạng cảnh báo trên tập dữ liệu có nhãn. So sánh với rule-based baseline về Recall@K, Precision@K và thời gian xử lý. Fraud Analyst hoặc người đánh giá được hướng dẫn có thể kiểm tra kết quả mà không thực hiện bất kỳ hành động nào trên tài khoản thật.

**Nếu Not Yet — cần kiểm chứng gì trước:**

- Xác minh nhu cầu và quy trình xử lý cảnh báo qua phỏng vấn người có kinh nghiệm phù hợp.
- Kiểm tra dataset, nhãn gian lận, mức mất cân bằng lớp và khả năng xây dựng đặc trưng.
- Đo hiệu quả rule-based baseline trước khi quyết định sử dụng ML.
- Thử nghiệm tốc độ xử lý và khả năng fallback.
- Xác định giới hạn sử dụng dữ liệu và phạm vi triển khai an toàn.

**Nếu No-Go — nên làm gì thay AI:**

Chuẩn hóa quy trình xử lý, xây dựng bộ lọc và bảng ưu tiên rule-based, bổ sung thông tin lịch sử giao dịch để Fraud Analyst dễ kiểm tra hơn.

**Ngưỡng dừng:**

Sau giai đoạn pilot offline, nếu ML không cải thiện Recall@K so với rule-based, làm giảm recall phát hiện gian lận, không đạt mục tiêu thời gian ≤10 giây/cảnh báo hoặc không đảm bảo fallback an toàn, nhóm dừng hướng ML và quay về rule-based.

Nếu chưa có dữ liệu đủ chất lượng để đánh giá, nhóm tạm dừng kết luận về hiệu quả ML cho đến khi có dữ liệu phù hợp.

---

## 9. Hạn chế và hướng tiếp theo

- **Hạn chế về kiểm chứng:** Nhóm chưa có phỏng vấn trực tiếp với Fraud Analyst thực tế, vì vậy các khó khăn và nhu cầu được xác định hiện vẫn cần xác minh.
- **Hạn chế về số liệu:** Khối lượng 500 cảnh báo/ngày, thời gian 5 phút/cảnh báo và phân bổ thời gian từng bước là giả định ban đầu. Mục tiêu ≤10 giây là chỉ tiêu kỹ thuật chưa được đo.
- **Hạn chế về dữ liệu:** Chưa xác nhận dataset có đủ thông tin lịch sử và nhãn để mô phỏng đầy đủ quy trình giám sát giao dịch trong môi trường thực tế.
- **Hạn chế về mô hình:** ML có thể gặp khó khăn với dữ liệu mất cân bằng, thay đổi hành vi gian lận và các trường hợp chưa xuất hiện trong dữ liệu huấn luyện.
- **Hướng tiếp theo:** Xây dựng rule-based baseline, thử nghiệm mô hình ML, đánh giá Recall@K, Precision@K, recall và thời gian xử lý. Sau đó xây dựng giao diện xếp hạng cảnh báo có HITL và fallback để kiểm chứng quy trình trước/sau.

## 10. Tài liệu tham khảo
1. Basel Committee on Banking Supervision (BCBS). Anti-money laundering and counter-terrorist financing — Basel Framework. https://www.bis.org/committees/bcbs/basel-consolidated-guidelines/module/afs/10
2. Wolfsberg Group (2024). Effective Monitoring for Suspicious Activity — Part I. https://wolfsberg-group.org/resources/general/168/
3. Wolfsberg Group. Effective Monitoring for Suspicious Activity — Part II. https://wolfsberg-group.org/resources/195/202
