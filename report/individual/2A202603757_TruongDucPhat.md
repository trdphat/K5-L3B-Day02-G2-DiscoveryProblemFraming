# Báo cáo cá nhân — 2A202603757_TruongDucPhat

> Đổi tên file theo quy tắc `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md` (MSSV trước, dấu `_`, họ tên viết liền không dấu). Sửa cả dòng tiêu đề phía trên cho khớp.
> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: copy template này thành file mới, điền, rồi commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên: Trương Đức Phát   
- MSSV: 2A202603757
- Email trường (không bắt buộc, repo có thể để public): 26ai.phattd@vinuni.edu.vn
- Tên nhóm: G2
- Link repo nhóm: https://github.com/trdphat/K5-L3B-Day02-G2-DiscoveryProblemFraming

---

## 2. Scan problem (CP1)

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

| # | Lăng kính | Job Story: Khi… tôi muốn… để… | Ai chịu ảnh hưởng? | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng) |
|---:|---|---|---|---|
| 1 | Lặp lại | Nhân viên kiểm tra thủ công hàng trăm giao dịch đáng ngờ | Khi hệ thống phát sinh cảnh báo gian lận, tôi muốn tự động đánh giá và ưu tiên các giao dịch rủi ro cao để giảm công việc kiểm tra thủ công | Fraud team | 500 cảnh báo/ngày, 5 phút/cảnh báo, 80% không cần xử lý thêm.
| 2 | Lặp lại | Phân loại thủ công khiếu nại của khách hàng | Khi phát sinh khiếu nại từ người dùng, tôi muốn hệ thống phân loại và chuyển đúng bộ phận | Customer Support | 2.000 tickets/ngày, 3 phút/ticket.
| 3 | Pain từ người khác| Khách hàng bị khóa giao dịch nhầm | Khi một giao dịch hợp lệ bị hệ thống đánh dấu gian lận, tôi muốn có cơ chế đánh giá lại tự động để tránh làm gián đoạn thanh toán. | Khách hàng, Fraud team | 15% giao dịch bị chặn phải xử lý khiếu nại.
| 4 | Pain từ người khác | Khách hàng bị lừa chuyển tiền | Khi khách hàng chuẩn bị chuyển tiền đến tài khoản có dấu hiệu lừa đảo, tôi muốn hệ thống cảnh báo rủi ro để hạn chế tổn thất. | Khách hàng, Risk Team, Customer Support | 100 vụ khiếu nại/tháng, phần lớn được báo cáo sau giao dịch.
| 5 | Decision Bottlenecks| Phê duyệt khoản vay chậm | Khi khách hàng đăng ký khoản vay, tôi muốn có hệ thống hỗ trợ chấm điểm tín dụng để đưa ra quyết định nhanh và nhất quán hơn. |Credit Team, khách hàng| 5.000 hồ sơ/tháng, 20% cần đánh giá thủ công.
| 6 | | | | |
| 7 | | | | |
| 8 | | | | |

**Nếu có dùng AI để gợi ý thêm:** ý nào AI gợi ý mà bạn giữ lại, ý nào bỏ và vì sao.
Loại bỏ ý 5: vì có thể phụ thuộc vào quy trình thực tế, business rule của từng tổ chức tín dụng.
Loại bỏ ý 3: vì có thể trùng nguyên nhân bài toán ý 1.

-

---

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 | Kiểm tra thủ công giao dịch đáng ngờ | Tần suất lặp lại cao (giả định 500 cảnh báo/ngày, 5 phút/cảnh báo), gây tốn thời gian và nguồn lực của Fraud Team. AI có thể hỗ trợ phân tích, chấm điểm và ưu tiên giao dịch rủi ro cao, giúp giảm khối lượng kiểm tra thủ công. | 80% cảnh báo không cần xử lý thêm có thực sự là cảnh báo sai không?. Dữ liệu giao dịch và kết quả điều tra có đủ chất lượng để huấn luyện AI không?. AI có thể giảm thời gian xử lý mà không bỏ sót gian lận không? |
| 2 | Phân loại thủ công khiếu nại khách hàng | Công việc có tính lặp lại cao (giả định 2.000 ticket/ngày, 3 phút/ticket), quy trình rõ ràng và dễ đo lường hiệu quả. AI có thể tự động phân loại và chuyển ticket đến đúng bộ phận, giúp giảm thời gian xử lý và tăng tốc độ phản hồi khách hàng. | Tỷ lệ ticket bị phân loại sai hiện tại là bao nhiêu? Dữ liệu ticket lịch sử có được gán nhãn đầy đủ không? AI có thực sự hiệu quả hơn hệ thống rule-based hiện tại không? |
| 3 | Cảnh báo khách hàng chuyển tiền lừa đảo | Gây thiệt hại trực tiếp về tài chính và ảnh hưởng đến uy tín công ty (giả định 100 khiếu nại/tháng). AI có tiềm năng phân tích hành vi và phát hiện giao dịch đáng ngờ trước khi hoàn tất chuyển tiền, từ đó hạn chế tổn thất cho khách hàng. | Có đủ dữ liệu về các giao dịch lừa đảo đã được xác minh không? AI có thể phát hiện rủi ro trước khi tiền được chuyển đi không? Làm thế nào để hạn chế cảnh báo sai gây ảnh hưởng trải nghiệm khách hàng? |

### Problem Card #1

| Trường | Nội dung |
|---|---|
| Job Story | Khi hệ thống phát sinh số lượng lớn cảnh báo giao dịch đáng ngờ, tôi muốn nhanh chóng xác định và ưu tiên những giao dịch có rủi ro cao để giảm thời gian kiểm tra thủ công mà không bỏ sót gian lận. |
| Actor | Fraud Analyst, Fraud Operations Team. |
| Thời điểm / bối cảnh | Trong quá trình giám sát giao dịch hằng ngày, đặc biệt vào giờ cao điểm hoặc khi lượng giao dịch tăng đột biến. |
| Quy trình hiện tại (3–7 bước) | 1. Hệ thống rule-based phát hiện giao dịch bất thường. 2. Tạo cảnh báo. 3. Fraud Analyst mở danh sách cảnh báo. 4. Tra cứu lịch sử giao dịch, thông tin tài khoản và thiết bị. 5. Đánh giá rủi ro, quyết định đóng cảnh báo hoặc chuyển điều tra. 6. Cập nhật kết quả xử lý. |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 4–5: trung bình 5 phút/cảnh báo. Với 500 cảnh báo/ngày, tổng khối lượng xử lý ước tính 2.500 phút/ngày (41,7 giờ công). |
| Impact (nếu không giải thì sao) | Tăng chi phí vận hành, tồn đọng cảnh báo, chậm xử lý các giao dịch rủi ro cao và có nguy cơ bỏ sót gian lận. |
| Success metric (baseline → target) | Thời gian xử lý trung bình: 5 → 2 phút/cảnh báo. Khối lượng xử lý thủ công: 41,7 → 16,7 giờ công/ngày (giả định số lượng cảnh báo không đổi). Fraud recall không thấp hơn baseline. |
| Phương án không dùng AI | Tối ưu ngưỡng cảnh báo, loại bỏ quy tắc trùng lặp, phân nhóm cảnh báo theo mức độ nghiêm trọng và xây dựng dashboard hỗ trợ tra cứu nhanh. |
| Giả thuyết về AI (nếu có) | ML Risk Scoring có thể phân tích lịch sử giao dịch, tần suất, thiết bị và hành vi để xếp hạng cảnh báo theo rủi ro, hỗ trợ Fraud Analyst ưu tiên kiểm tra.|
| Cảm nhận nhanh | Rule / Workflow → AI hỗ trợ (chưa cần Agent tự quyết định). |

Quy trình nháp hiện tại:


[1] Khách hàng thực hiện giao dịch -->[2] Hệ thống Rule-based kiểm tra giao dịch --> [3] Phát hiện bất thường và tạo cảnh báo --> [4] Fraud Analyst tiếp nhận cảnh báo --> [5] Tra cứu lịch sử giao dịch, tài khoản, thiết bị và hành vi người dùng --> [6] Đánh giá mức độ rủi ro thủ công (bottleneck) --> [7] Quyết định xử lý --> [8] Ghi nhận kết quả vào hệ thống



### Problem Card #2

| Trường | Nội dung |
|---|---|
| Job Story | Khi khách hàng gửi yêu cầu hỗ trợ hoặc khiếu nại, tôi muốn ticket được phân loại và chuyển đến đúng bộ phận nhanh chóng để giảm thời gian chờ xử lý và tránh chuyển sai tuyến. |
| Actor | Customer Support Agent, Customer Support Supervisor và khách hàng.|
| Thời điểm / bối cảnh | Khi ticket được gửi từ ứng dụng, email hoặc live chat, đặc biệt trong những khung giờ cao điểm. |
| Quy trình hiện tại (3–7 bước) | 1. Khách hàng gửi yêu cầu hỗ trợ. 2. Hệ thống CRM tạo ticket. 3. Nhân viên đọc nội dung. 4. Xác định loại vấn đề và mức độ ưu tiên. 5. Chọn bộ phận phụ trách, chuyển ticket. 6. Bộ phận nhận tiếp tục xử lý hoặc chuyển lại nếu sai tuyến.|
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3–5: trung bình 3 phút/ticket. Với 2.000 ticket/ngày, tương đương 6.000 phút (100 giờ công/ngày) dành cho phân loại và chuyển tuyến. |
| Impact (nếu không giải thì sao) | Tăng thời gian phản hồi khách hàng, tồn đọng ticket, tăng chi phí nhân sự, có nguy cơ vi phạm SLA và giảm mức độ hài lòng của người dùng. |
| Success metric (baseline → target) | 	Thời gian phân loại: 3 phút → dưới 30 giây/ticket. Độ chính xác phân tuyến: baseline chưa xác định → mục tiêu ≥ 95% trên tập đánh giá. Theo dõi thêm tỷ lệ chuyển sai tuyến và SLA. |
| Phương án không dùng AI | Chuẩn hóa danh mục ticket, thiết lập form có lựa chọn loại vấn đề, quy tắc phân tuyến dựa trên danh mục, từ khóa và tài khoản phụ trách. |
| Giả thuyết về AI (nếu có) | có thể hiểu nội dung khiếu nại, đề xuất category, priority và bộ phận phụ trách; các ticket không chắc chắn được chuyển cho nhân viên xác nhận. |
| Cảm nhận nhanh | Workflow  |

Quy trình nháp hiện tại:

[1] Khách hàng gửi khiếu nại (App / Email / Live Chat) --> [2] Hệ thống CRM tạo ticket --> [3] Customer Support tiếp nhận ticket --> [4] Nhân viên đọc và phân tích nội dung --> [5] Xác định loại khiếu nại, mức độ ưu tiên và bộ phận phụ trách (bottleneck) --> [6] Chuyển ticket đến bộ phận liên quan --> [7] Bộ phận tiếp nhận kiểm tra --> [8] Cập nhật trạng thái và phản hồi khách hàng


### Problem Card #3

| Trường | Nội dung |
|---|---|
| Job Story | Khi chuẩn bị chuyển tiền đến một tài khoản có dấu hiệu lừa đảo, tôi muốn được cảnh báo rủi ro kịp thời để cân nhắc lại giao dịch và tránh mất tiền. |
| Actor | 	Khách hàng sử dụng ứng dụng Fintech; Risk/Fraud Team là bộ phận hỗ trợ kiểm soát rủi ro. |
| Thời điểm / bối cảnh | Khi khách hàng nhập thông tin người nhận và số tiền, trước bước xác nhận chuyển khoản.|
| Quy trình hiện tại (3–7 bước) | 1. Khách hàng mở chức năng chuyển tiền. 2. Nhập tài khoản nhận và số tiền. 3. Hệ thống kiểm tra thông tin và các quy tắc rủi ro cơ bản. 4. Khách hàng xác nhận giao dịch. 5. Hệ thống thực hiện chuyển tiền. 6. Nếu phát hiện bị lừa, khách hàng liên hệ hỗ trợ để tra soát. |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3: hệ thống chưa có đủ tín hiệu để nhận diện tài khoản nhận tiền có dấu hiệu lừa đảo. Bước 6: quy trình hỗ trợ giả định mất 15–30 phút tiếp nhận và xác minh ban đầu mỗi vụ, trong khi tiền đã được chuyển. |
| Impact (nếu không giải thì sao) | Khách hàng có nguy cơ mất tiền, khó thu hồi tài sản, giảm niềm tin vào nền tảng và gia tăng chi phí tra soát, hỗ trợ khiếu nại. |
| Success metric (baseline → target) | 	Số khiếu nại lừa đảo: 100 → dưới 70 vụ/tháng. Tỷ lệ phát hiện giao dịch lừa đảo đã xác minh trước chuyển tiền: baseline chưa biết → mục tiêu pilot ≥ 70%. Đồng thời theo dõi tỷ lệ cảnh báo sai và số tiền thiệt hại. |
| Phương án không dùng AI | Danh sách tài khoản bị báo cáo, kiểm tra người nhận mới, cảnh báo khi chuyển số tiền lớn, xác nhận bổ sung đối với giao dịch có rủi ro và hướng dẫn nhận diện lừa đảo. |
| Giả thuyết về AI (nếu có) | 	ML kết hợp Graph Analytics có thể nhận diện tài khoản nhận tiền có hành vi bất thường, phân tích mạng lưới giao dịch và đưa ra cảnh báo dựa trên mức độ rủi ro trước khi chuyển tiền |
| Cảm nhận nhanh | Rule|

Quy trình nháp hiện tại:

[1] Khách hàng mở chức năng chuyển tiền --> [2] Nhập tài khoản nhận và số tiền -->   [3] Hệ thống kiểm tra thông tin người nhận và các quy tắc rủi ro cơ bản --> [4] Không phát hiện dấu hiệu cần ngăn chặn --> [5] Khách hàng xác nhận giao dịch --> [6] Hệ thống thực hiện chuyển tiền --> [7] Khách hàng phát hiện mình bị lừa (botteneck) --> [8] Liên hệ Customer Support --> [9] Nhân viên tiếp nhận và xác minh --> [10] Chuyển Fraud/Risk Team để tra soát, phối hợp xử lý và hỗ trợ thu hồi tiền


### Card muốn pitch nhất

- Card số: 1
- Vì sao: Khối lượng 500 cảnh báo/ngày ngốn 41.7 giờ công xử lý thủ công (tương đương 5-6 nhân sự full-time chỉ để làm nhiệm vụ tra cứu và lọc cảnh báo). Bottleneck cực kỳ lớn ở bước 4–5.
- Câu hỏi muốn nhóm phản biện:

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|---|---|---|
|Rule-based thiếu khả năng chấm điểm rủi ro linh hoạt, dẫn đến quá tải 500 cảnh báo/ngày mà không phân loại được độ khẩn cấp. | Đồng ý | Tái cấu trúc bước tra cứu: Tích hợp màn hình xem nhanh, tập trung thông tin lịch sử, thiết bị, và lý do AI gợi ý điểm rủi ro để Analyst đưa ra quyết định ngay. |

---

## 4. Tôi đã tham gia phần nào (CP3 → CP7)

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch Problem Card | Tôi đề xuất candidate problem: (1) Ưu tiên cảnh báo giao dịch đáng ngờ, (2) Tự động phân loại và điều phối ticket CSKH, (3) Cảnh báo tài khoản có dấu hiệu lừa đảo trước khi chuyển tiền. Xác định actor, job story, bottleneck và impact của từng bài toán. | Bổ sung 3 bài toán liên quan đến Fintech và chăm sóc khách hàng. Candidate #1 được nhóm lựa chọn để nghiên cứu. |
| Phản biện bài của bạn khác | Câu hỏi tôi đã đặt: cách thu thập thông tin từ nhóm chat (#4), cách tổng hợp bài giảng khi thiếu tài liệu (#8) và khả năng theo dõi tiến độ khi thành viên không cập nhật (#6).|  Giúp nhóm xem xét tính khả thi và những giới hạn về dữ liệu đầu vào của các candidate. |
| Nhận phản biện | Câu hỏi tôi nhận được: Tôi nhận được câu hỏi về nguy cơ bỏ sót gian lận khi ưu tiên sai (#1), khả năng phân loại ticket khi khách hàng mô tả không rõ (#2) và ảnh hưởng của cảnh báo nhầm đến niềm tin khách hàng (#3)| Tôi đã sửa gì: Làm rõ các rủi ro về độ chính xác, False Negative và False Positive khi ứng dụng AI.|
| Gom cluster / cây OST | Tôi tham gia tổng hợp 12 candidate thành 3 cluster, xác định các Opportunity và phân biệt chúng với những giải pháp như Rule, ML hoặc OCR.| Nhóm xây dựng cây OST với mục tiêu giảm thời gian xử lý thủ công và hạn chế sai sót.|
| Chọn candidate problem | Tôi trình bày Candidate #1, phân tích actor, bottleneck và khả năng đánh giá hiệu quả bằng thời gian xử lý và chất lượng ưu tiên. | Candidate #1 đạt 31/35 điểm, được nhóm thống nhất lựa chọn. |  Candidate #1 đạt 31/35 điểm, được nhóm thống nhất lựa chọn.|
| Kiểm chứng / research | Tôi phụ trách xây dựng Assumption Map, tập trung vào khối lượng cảnh báo, khó khăn khi xác định thứ tự ưu tiên và nguy cơ xử lý chậm. Tôi tổng hợp các Interview Snapshot và nghiên cứu tài liệu Basel Committee, Wolfsberg Group.| Nhóm xác định 3 giả định cần ưu tiên kiểm chứng, làm rõ nhu cầu hỗ trợ Fraud Analyst và lựa chọn hướng nghiên cứu Rule kết hợp ML. |
| Quy trình nhóm |Tôi góp ý về các bước xử lý cảnh báo hiện tại, đặc biệt là việc kiểm tra lịch sử và xác định thứ tự ưu tiên.  |Giúp nhóm xác định bottleneck và xây dựng cơ sở cho quy trình Before/After |
| Problem Statement | Tôi tham gia làm rõ actor, bottleneck và impact dựa trên kết quả kiểm chứng và research.| Problem Statement tập trung vào việc giảm thời gian rà soát và hạn chế xử lý chậm cảnh báo rủi ro cao.|
| Mức can thiệp AI |Tôi góp ý về khả năng áp dụng Rule và ML Risk Scoring dựa trên các phương pháp giám sát giao dịch đã nghiên cứu. |Nhóm lựa chọn Rule làm baseline và chỉ thử nghiệm ML khi có khả năng cải thiện hiệu quả. |
| Quyết định |Tôi tham gia đánh giá Value Risk, đặc biệt là nhu cầu thực tế của Fraud Analyst và mức độ bằng chứng hiện có.  | |
 Góp phần vào quyết định Not Yet, ưu tiên kiểm chứng và xây dựng prototype trước khi triển khai thực tế. 
---

## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| **CP1 Scan** | Em dùng AI để gợi ý các vấn đề thực tế trong lĩnh vực Fintech, đặc biệt là phát hiện gian lận và chăm sóc khách hàng. | Giúp em tìm được nhiều hướng bài toán và nhận ra những công việc đang mất nhiều thời gian xử lý thủ công. | Một số ý tưởng còn chung chung, chưa chỉ rõ ai gặp vấn đề và vấn đề xảy ra ở bước nào. | Em chọn lại 3 bài toán có đối tượng sử dụng và quy trình tương đối rõ để phân tích sâu hơn. |
| **CP2 Problem Card** | Em nhờ AI hỗ trợ viết Job Story, xác định Actor, Bottleneck và gợi ý cách đo lường hiệu quả cho 3 Problem Card. | Giúp em sắp xếp ý tưởng theo đúng cấu trúc và trình bày vấn đề dễ hiểu hơn. | AI đưa ra một số con số về thời gian xử lý và khối lượng công việc nhưng chưa có nguồn kiểm chứng. | Em xem các số liệu này là giả định ban đầu, đồng thời xác định lại bước nào thực sự gây mất thời gian trong quy trình. |
| **CP4 Research** | Em dùng AI để tìm hiểu các cách ưu tiên cảnh báo gian lận, như rule-based và ML Risk Scoring, cũng như gợi ý các tiêu chí đánh giá. | Giúp em hiểu điểm khác nhau giữa các cách xử lý và những chỉ số cần quan tâm khi thử nghiệm. | AI thường nói ML có thể cải thiện hiệu quả nhưng chưa chứng minh được mức cải thiện cụ thể trên dữ liệu của nhóm. | Em đề xuất so sánh các phương án trên cùng bộ dữ liệu thử nghiệm thay vì kết luận ML tốt hơn ngay từ đầu. |
| **CP5 Quy trình** | Em dùng AI để hỗ trợ xây dựng quy trình trước và sau khi áp dụng AI, xác định bước nào dùng Rule, ML và con người xử lý. | Giúp em hình dung rõ hơn cách đưa AI vào quy trình hiện tại mà không cần thay đổi toàn bộ cách làm việc. | Ban đầu AI có xu hướng tự động hóa nhiều bước, chưa tính kỹ trường hợp dự đoán sai hoặc hệ thống gặp lỗi. | Em bổ sung bước Fraud Analyst kiểm tra và phương án quay về rule-based nếu AI lỗi hoặc dữ liệu không hợp lệ. |
| **CP5–6 Problem Statement** | Em nhờ AI hỗ trợ tổng hợp Actor, Bottleneck, Impact, Success Metric và Boundary để viết Problem Statement. | Giúp em diễn đạt vấn đề ngắn gọn hơn và liên kết được điểm nghẽn với kết quả cần cải thiện. | Một số mục tiêu AI đề xuất khá lý tưởng, chưa dựa trên kết quả thử nghiệm thực tế. | Em điều chỉnh lại cách trình bày, phân biệt số liệu ước tính với kết quả đã kiểm chứng và nhấn mạnh việc không được bỏ sót cảnh báo. |
| **CP6 Mức can thiệp / quyết định** | Em dùng AI để so sánh các mức No AI, Rule, Workflow và Agent, đồng thời xem xét các rủi ro khi triển khai. | Giúp em thấy được ưu, nhược điểm của từng mức và những vấn đề cần kiểm tra trước khi áp dụng thực tế. | AI có xu hướng đề xuất giải pháp phức tạp hơn mức cần thiết và chưa đánh giá đầy đủ rủi ro về dữ liệu, độ chính xác. | Em nghiêng về Workflow kết hợp Rule + ML + Human-in-the-Loop thay vì Agent. Em cũng tham gia đánh giá tính khả thi và thống nhất với nhóm chọn Not Yet để kiểm chứng thêm trước khi triển khai. |

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5). **Không dùng AI để viết thay.**

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**
  Khi nghe các bạn trình bày, em nhận ra rằng một bài toán tốt không nhất thiết phải sử dụng công nghệ phức tạp mà quan trọng là xác định đúng vấn đề cần giải quyết
**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**
  Với bài toán của em, ban đầu em cũng tập trung vào việc dùng ML để phân loại và ưu tiên cảnh báo giao dịch. Tuy nhiên, khi xây dựng cây OST, nhóm đã phân biệt lại đâu là vấn đề thực tế và đâu chỉ là giải pháp đề xuất. Từ đó, nhóm tập trung vào bottleneck là thời gian kiểm tra cảnh báo thủ công trước khi lựa chọn công nghệ phù hợp.
**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**
  Em nhận được câu hỏi rằng nếu hệ thống ưu tiên sai thì có thể bỏ sót giao dịch gian lận thật hay không. Câu hỏi này khiến em phải xem xét lại việc sử dụng ML để xếp hạng cảnh báo. Thay vì chỉ quan tâm đến tốc độ xử lý, em nhận ra cần chú trọng cả độ chính xác và hậu quả khi mô hình dự đoán sai. Vì vậy, hướng em đề xuất là giữ lại tất cả cảnh báo, sử dụng AI để hỗ trợ sắp xếp mức độ ưu tiên và để Fraud Analyst kiểm tra, quyết định cuối cùng.
**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**
  Một giải pháp sử dụng AI chưa chắc đã hiệu quả hơn cách xử lý truyền thống. Ban đầu, em nghĩ việc sử dụng ML để đánh giá và ưu tiên các cảnh báo giao dịch sẽ giúp giảm đáng kể thời gian xử lý. Tuy nhiên, khi xem xét kỹ hơn, em nhận ra nếu mô hình dự đoán sai thì có thể khiến những giao dịch gian lận thực sự bị xếp vào nhóm ưu tiên thấp. 
**6.5. Điều khó nhất khi viết Problem Statement là gì?**
  Khó nhất là diễn đạt đúng vấn đề mà không đưa giải pháp vào quá sớm. Ban đầu, em dễ tập trung vào việc xây dựng hệ thống ML để phát hiện hoặc ưu tiên giao dịch gian lận. Tuy nhiên, vấn đề thực sự của Fraud Analyst là phải xử lý số lượng lớn cảnh báo trong khi thời gian và nguồn lực có hạn. Ngoài ra, việc xác định Success Metric cũng khá khó vì cần có số liệu thực tế để làm baseline.
**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**
  Nếu làm lại, em sẽ dành nhiều thời gian hơn cho việc kiểm chứng vấn đề trước khi nghĩ đến giải pháp. Đặc biệt, em muốn tìm hiểu rõ quy trình xử lý cảnh báo thực tế của Fraud Analyst và có dữ liệu cụ thể về thời gian xử lý, số lượng cảnh báo cũng như tỷ lệ cảnh báo sai. Khi phản biện các bài toán của nhóm, em sẽ tập trung hơn vào nguồn dữ liệu, tính khả thi và cách đo lường hiệu quả.
**6.7. Hiểu bài:** giải thích bằng 5–8 câu, không nhìn tài liệu, chuỗi *problem → quy trình → metric → boundary → mức can thiệp AI → quyết định* của bài nhóm mình.
  việc Fraud Analyst phải kiểm tra nhiều cảnh báo giao dịch đáng ngờ, dẫn đến mất thời gian và có nguy cơ bỏ sót gian lận. Trong quy trình hiện tại, nhân viên phải xem xét và xác minh từng cảnh báo trước khi đưa ra quyết định xử lý. Nhóm muốn cải thiện thời gian xử lý và khả năng ưu tiên cảnh báo thông qua các chỉ số như thời gian kiểm tra, tỷ lệ phát hiện gian lận và tỷ lệ cảnh báo sai. Tuy nhiên, AI chỉ được hỗ trợ đánh giá mức độ rủi ro, không được tự ý loại bỏ cảnh báo hoặc quyết định giao dịch có gian lận hay không. Vì vậy, nhóm lựa chọn Workflow kết hợp Rule, ML và Human-in-the-Loop thay vì sử dụng Agent tự động. Khi AI gặp lỗi hoặc dữ liệu không hợp lệ, hệ thống có thể quay về xử lý bằng rule-based và chuyển cho con người kiểm tra.
---

## 7. Tài liệu tham khảo

-
