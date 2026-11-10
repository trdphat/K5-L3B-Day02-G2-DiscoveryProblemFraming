# Team

## Thông tin nhóm

- **Tên nhóm:** G2
- **Candidate problem nhóm chọn:** Ưu tiên cảnh báo giao dịch đáng ngờ, giúp Fraud Analyst xác định các giao dịch rủi ro cao cần kiểm tra trước.
- **Quyết định cuối:** Not Yet

## Thành viên

| STT | Họ và tên | MSSV | Vai trò trong nhóm | Tài khoản GitHub |
|---:|---|---|---|---|
| 1 | Trương Đức Phát | 2A202603757 | Điều phối nhóm, hội tụ vấn đề, phụ trách research | trdphat |
| 2 | Đào Nguyễn Quang Thành |2A202603754 | Phân tích và xây dựng quy trình Before/After | ThanhDao11 |
| 3 | Hồ An Lộc |2A202603743 | Phụ trách kiểm chứng, Problem Statement và Success Metric |  hal2332004 |
| 4 | Nguyễn Minh Nhân | A2202603723 | Phản biện, phân tích mức can thiệp AI, AI Canvas và đánh giá rủi ro | uscalurn |

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

### TruongDucPhat-2A202603757

**Phần việc phụ trách:**

- Đề xuất và phản biện các Candidate Problem trong lĩnh vực Fintech và chăm sóc khách hàng.
- Phân tích Actor, Job Story, Bottleneck, Impact và Success Metric; tham gia xây dựng cây Opportunity Solution Tree (OST).
- Tham gia lựa chọn và kiểm chứng Candidate Problem, xây dựng Assumption Map và tổng hợp tài liệu nghiên cứu.
- Góp ý quy trình Before/After, mức can thiệp AI, Problem Statement và đánh giá rủi ro trước khi triển khai.

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):

- Đề xuất ba Candidate Problem: ưu tiên cảnh báo giao dịch đáng ngờ (#1), tự động phân loại và điều phối ticket chăm sóc khách hàng (#2), cảnh báo tài khoản có dấu hiệu lừa đảo trước khi chuyển tiền (#3).
- Xây dựng ba Problem Card với Job Story, Actor, Bottleneck, Impact, Success Metric, phương án không dùng AI và giả thuyết ứng dụng AI; mô tả quy trình hiện tại của từng bài toán.
- Phản biện các Candidate #4, #6, #8 về khả năng thu thập thông tin nhóm chat, theo dõi tiến độ thành viên và tổng hợp bài giảng khi thiếu dữ liệu đầu vào.
- Tiếp nhận phản biện về nguy cơ bỏ sót gian lận (#1), phân loại sai ticket (#2) và tác động của cảnh báo nhầm (#3); bổ sung phân tích False Negative và False Positive.
- Tham gia tổng hợp 12 Candidate Problem thành ba cluster, xây dựng cây OST và phân biệt Opportunity với các giải pháp Rule, ML hoặc OCR.
- Trình bày và phân tích Candidate #1 về kiểm tra thủ công giao dịch đáng ngờ; Candidate được nhóm lựa chọn với kết quả đánh giá 31/35 điểm.
- Xây dựng Assumption Map, xác định các giả định cần kiểm chứng và tổng hợp Interview Snapshot cùng tài liệu tham khảo từ Basel Committee và Wolfsberg Group.
- Góp ý quy trình Before/After, xác định bottleneck tại bước tra cứu, đánh giá và ưu tiên cảnh báo; đề xuất kết hợp Rule + ML Risk Scoring + Human-in-the-Loop.
- Tham gia xây dựng Problem Statement, làm rõ Actor, Bottleneck, Impact, Success Metric và Boundary; nhấn mạnh AI chỉ hỗ trợ ưu tiên, không tự động loại bỏ cảnh báo hoặc thay thế quyết định của Fraud Analyst.
- So sánh các mức can thiệp No AI, Rule, Workflow và Agent; đề xuất sử dụng Rule làm baseline, chỉ thử nghiệm ML khi có bằng chứng cải thiện hiệu quả.
- Tham gia đánh giá Value Risk và thống nhất quyết định Not Yet, ưu tiên kiểm chứng giả định và xây dựng prototype trước khi triển khai thực tế.

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):

- `report/individual/2A202603757_TruongDucPhat.md` — Mục 2: Đề xuất các Candidate Problem #1–#5, lựa chọn và loại bỏ những ý tưởng chưa phù hợp.
- `report/individual/2A202603757_TruongDucPhat.md` — Mục 3: Xây dựng Top 3 Problem Cards (#1, #2, #3), xác định bottleneck, Success Metric và quy trình nháp.
- `report/individual/2A202603757_TruongDucPhat.md` — Mục 4: Ghi nhận các đóng góp từ CP3–CP7, bao gồm phản biện Candidate, xây dựng OST, Assumption Map, research, Before/After, Problem Statement và quyết định Not Yet.
- `report/individual/2A202603757_TruongDucPhat.md` — Mục 5: Trình bày việc sử dụng AI trong từng checkpoint, các hạn chế phát hiện được và cách điều chỉnh bằng nhận định cá nhân.
- `report/individual/2A202603757_TruongDucPhat.md` — Mục 6: Reflection về quá trình xác định vấn đề, tiếp nhận phản biện, kiểm chứng giả định, lựa chọn mức can thiệp AI và đánh giá rủi ro.

**Điều mình học được từ phần nhóm:**

- Em học được rằng việc xác định đúng vấn đề và kiểm chứng các giả định quan trọng hơn việc lựa chọn công nghệ ngay từ đầu. Qua quá trình phản biện, em nhận ra AI không phải lúc nào cũng tốt hơn Rule-based, đặc biệt với bài toán phát hiện gian lận, nơi một dự đoán sai có thể gây hậu quả nghiêm trọng. Vì vậy, cần đánh giá đồng thời hiệu quả xử lý, độ chính xác, rủi ro và giới hạn tự động hóa. Em cũng hiểu rõ hơn vai trò của Human-in-the-Loop, cách xây dựng Success Metric và Boundary, cũng như lý do cần lựa chọn Not Yet khi chưa có đủ bằng chứng để triển khai thực tế.

### DaoNguyenQuangThanh-2A202603754

**Phần việc phụ trách:**

- Đề xuất và phân tích các Candidate Problem liên quan đến học tập, thực tập và quản lý thông tin.
- Phản biện các Candidate Problem của thành viên khác, làm rõ bottleneck, tính khả thi và giới hạn dữ liệu đầu vào.
- Tham gia xây dựng Opportunity Solution Tree (OST), đặc biệt là Opportunity B.
- Tổng hợp và kiểm tra bảng đánh giá, chấm điểm các Candidate Problem để hỗ trợ nhóm lựa chọn bài toán phù hợp.

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):

- Đề xuất năm vấn đề trong bối cảnh sinh viên vừa học vừa thực tập, bao gồm quản lý chi tiêu cá nhân, ưu tiên ôn thi, điều chỉnh CV khi ứng tuyển, tìm lại bối cảnh nhiệm vụ/dự án và tổng hợp nội dung học tập sau khi nghỉ học.
- Xây dựng ba Problem Card: tìm lại bối cảnh nhiệm vụ/dự án (#4), bù bài sau khi nghỉ học (#8 theo danh sách Candidate nhóm, cần đối chiếu) và ưu tiên ôn tập (#9 theo danh sách Candidate nhóm, cần đối chiếu); xác định Job Story, Actor, Bottleneck, Impact, Success Metric và phương án không sử dụng AI.
- Phản biện Candidate của TruongDucPhat về nguy cơ cảnh báo nhầm làm giảm niềm tin khách hàng; Candidate của HoAnLoc về việc thành viên không cập nhật tiến độ; Candidate của NguyenMinhNhan về xác định chính xác ngày hết hạn khi hợp đồng có nhiều mốc thời gian.
- Tiếp nhận phản biện về mâu thuẫn giữa nguồn chat và tài liệu, thiếu dữ liệu bài giảng và tính chủ quan khi đánh giá độ khó bài tập; điều chỉnh Problem Card theo hướng ưu tiên nguồn chính thức, chỉ tổng hợp thông tin có căn cứ và không suy đoán dữ liệu.
- Phân tích nhóm vấn đề tìm kiếm, tra cứu và tổng hợp thông tin từ nhiều nguồn, góp phần xây dựng Opportunity B trong cây OST.
- Tổng hợp bảng đánh giá ba Candidate #1, #5 và #10 theo bảy tiêu chí; kiểm tra tổng điểm nhằm đảm bảo tính chính xác, nhất quán và hỗ trợ nhóm thống nhất lựa chọn Candidate #1.
- Xem xét phương án không dùng AI, như chuẩn hóa lưu trữ tài liệu, tìm kiếm theo từ khóa, sử dụng checklist và quy trình xác minh thông tin trước khi đề xuất ứng dụng AI.

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):

- `report/individual/2A202603754_DaoNguyenQuangThanh.md` — Mục 2: Đề xuất năm vấn đề thực tế liên quan đến học tập, thực tập và quản lý thông tin.
- `report/individual/2A202603754_DaoNguyenQuangThanh.md` — Mục 3: Xây dựng Top 3 Problem Cards, phân tích bottleneck, Success Metric, quy trình nháp và phản biện các giả thuyết AI.
- `report/individual/2A202603754_DaoNguyenQuangThanh.md` — Mục 4: Ghi nhận hoạt động phản biện các thành viên, tiếp nhận và điều chỉnh sau phản biện, xây dựng Opportunity B và tổng hợp bảng chấm điểm ba Candidate.
- `group_report.md` — Cần đối chiếu các mục tổng hợp Candidate Problem, cây OST và bảng đánh giá shortlist để xác định vị trí bằng chứng chính xác.

**Điều mình học được từ phần nhóm:**

- Qua quá trình xây dựng và phản biện các Candidate Problem, em nhận ra rằng cần xác định rõ vấn đề, đối tượng chịu ảnh hưởng và điểm nghẽn trong quy trình trước khi nghĩ đến giải pháp AI. Em cũng hiểu rằng chất lượng dữ liệu đầu vào và độ tin cậy của nguồn thông tin ảnh hưởng trực tiếp đến tính khả thi của giải pháp. Việc phản biện và tiếp nhận ý kiến từ các thành viên giúp em nhìn nhận vấn đề từ nhiều góc độ, điều chỉnh các giả định chưa có căn cứ và hiểu rõ hơn tầm quan trọng của việc đánh giá, so sánh các phương án theo tiêu chí thống nhất trước khi lựa chọn bài toán triển khai.

### HoAnLoc-2A202603743

**Phần việc phụ trách:**

- Đề xuất và phản biện các Candidate Problem liên quan đến học tập, quản lý deadline và xử lý thông tin.
- Tham gia xây dựng cây Opportunity Solution Tree (OST), phân nhóm Candidate và đánh giá shortlist.
- Phụ trách hoàn thiện Problem Statement v0 và v1, xác định Actor, Bottleneck, Impact, Success Metric, Boundary và AI intervention point.
- Tham gia xây dựng tiêu chí đánh giá giải pháp Rule + ML, xác định cơ chế fallback và điều kiện quyết định triển khai.

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):

- Đề xuất ba Candidate Problem: tổng hợp lịch học và deadline (#4), đọc và tổng hợp tài liệu học thuật (#5), theo dõi tiến độ bài tập nhóm (#6); xây dựng Problem Card với Job Story, Actor, Bottleneck, Impact, Success Metric và quy trình nháp.
- Phản biện Candidate #2 về khả năng phân loại ticket khi khách hàng mô tả không rõ ràng, Candidate #7 về xử lý thông tin mâu thuẫn giữa chat và tài liệu, Candidate #10 về hiệu quả OCR khi vẫn cần kiểm tra lại thủ công.
- Tiếp nhận phản biện về quyền truy cập tin nhắn, độ chính xác khi tóm tắt tài liệu và sự phụ thuộc vào ý thức cập nhật tiến độ; bổ sung Boundary, cơ chế trích dẫn nguồn và xác định những trường hợp không cần AI.
- Tham gia tổng hợp 12 Candidate thành ba cluster: Xử lý & phân loại, Tìm kiếm & tổng hợp, Quản lý công việc; xây dựng cây OST và phân biệt Opportunity với Solution.
- Tham gia chấm điểm ba Candidate trong shortlist theo bảy tiêu chí; Candidate #5 đạt 30 điểm, đứng trong Top 2 nhưng thống nhất lựa chọn Candidate #1 đạt 31 điểm do có tiêu chí đánh giá và khả năng thử nghiệm rõ ràng hơn.
- Rà soát các giả định về nhu cầu ưu tiên cảnh báo và khả năng đánh giá mô hình trên dữ liệu có nhãn; phân biệt số liệu giả định với bằng chứng đã kiểm chứng.
- Góp ý quy trình Before/After, phân biệt thời gian sàng lọc tự động (≤10 giây) và thời gian xử lý toàn quy trình (≤170 giây/cảnh báo).
- Phụ trách hoàn thiện Problem Statement v0 và v1, làm rõ Actor, Bottleneck, Impact, Success Metric, Boundary và vị trí AI can thiệp vào quy trình.
- Xây dựng tiêu chí đánh giá gồm Recall@K, recall phát hiện gian lận, thời gian xử lý và khả năng fallback; đề xuất Recall@K tăng tối thiểu 5 điểm phần trăm so với Rule-based baseline, p95 sàng lọc ≤10 giây và giữ lại 100% cảnh báo khi fallback.
- Tham gia xác định điều kiện dừng thử nghiệm ML nếu không cải thiện chất lượng ưu tiên so với Rule-based; góp phần đưa ra quyết định Not Yet khi chưa đủ bằng chứng triển khai thực tế.

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):

- `report/individual/2A202603743_HoAnLoc.md` — Mục 2: Đề xuất bảy vấn đề ban đầu từ trải nghiệm học tập và quản lý công việc.
- `report/individual/2A202603743_HoAnLoc.md` — Mục 3: Xây dựng Top 3 Problem Cards, phân tích quy trình, bottleneck, Success Metric và phương án không sử dụng AI.
- `report/individual/2A202603743_HoAnLoc.md` — Mục 4: Ghi nhận hoạt động pitch, phản biện, xây dựng OST, đánh giá shortlist, kiểm chứng giả định, hoàn thiện Problem Statement và đề xuất tiêu chí đánh giá AI.
- `report/individual/2A202603743_HoAnLoc.md` — Mục 5: Trình bày quá trình sử dụng AI, phát hiện hạn chế và điều chỉnh giải pháp tại các checkpoint.
- `report/individual/2A202603743_HoAnLoc.md` — Mục 6: Reflection về việc tránh solution-first, tiếp nhận phản biện, xây dựng Success Metric, Boundary và lựa chọn Not Yet.
- `group_report.md` — Cần đối chiếu các mục OST, bảng shortlist, quy trình Before/After, Problem Statement v0/v1 và đánh giá mức can thiệp AI để bổ sung vị trí bằng chứng chính xác.

**Điều mình học được từ phần nhóm:**

- Em học được rằng cần phân biệt rõ vấn đề thực tế với giải pháp công nghệ, tránh tư duy solution-first khi chưa hiểu đầy đủ quy trình và nhu cầu người dùng. Quá trình phản biện giúp em nhận ra không phải vấn đề nào cũng cần AI, đặc biệt khi nguyên nhân nằm ở cách tổ chức công việc hoặc hành vi con người. Khi xây dựng Problem Statement, em hiểu rõ hơn tầm quan trọng của Success Metric, Boundary và cơ chế fallback để đảm bảo AI hỗ trợ đúng vai trò mà không thay thế quyết định của Fraud Analyst. Em cũng nhận ra rằng cần kiểm chứng dữ liệu và hiệu quả thực tế trước khi triển khai, thay vì lựa chọn ML chỉ vì công nghệ này có tiềm năng.

