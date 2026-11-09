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
