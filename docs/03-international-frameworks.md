# Framework quốc tế dùng trong lab

Lab này không phát minh phương pháp mới. Mỗi kỹ thuật đều lấy từ một framework được dùng rộng rãi trong ngành product và thiết kế AI. Biết tên gốc giúp bạn đọc thêm tài liệu tiếng Anh và nói cùng ngôn ngữ với các team product quốc tế.

## Bản đồ framework theo checkpoint

| CP | Kỹ thuật trong lab | Framework gốc | Tác giả / tổ chức | Đọc thêm |
|---|---|---|---|---|
| Toàn bài | Mở rộng (Discover) rồi thu hẹp (Define) | **Double Diamond** | Design Council (UK) | [Framework for Innovation](https://www.designcouncil.org.uk/resources/framework-for-innovation/) |
| CP1–CP2 | Viết problem dạng "Khi… tôi muốn… để…" | **Jobs-to-be-Done / Job Story** | Intercom, Alan Klement | [How we accidentally invented Job Stories](https://www.intercom.com/blog/accidentally-invented-job-stories/) |
| CP3 | Cây outcome → opportunity → solution | **Opportunity Solution Tree** | Teresa Torres, *Continuous Discovery Habits* | [Opportunity Solution Trees](https://www.producttalk.org/opportunity-solution-trees/) |
| CP4 | Liệt kê và xếp hạng giả định | **Assumptions Mapping** | David Bland, *Testing Business Ideas* (cùng Alexander Osterwalder) | [Strategyzer: Assumptions mapping](https://www.strategyzer.com/library/how-assumptions-mapping-can-focus-your-teams-on-running-experiments-that-matter) |
| CP4 | Phỏng vấn về hành vi đã xảy ra, không hỏi giả định | **The Mom Test** | Rob Fitzpatrick | [momtestbook.com](https://www.momtestbook.com/) |
| CP4 | Ghi mỗi buổi phỏng vấn thành 1 trang | **Interview Snapshot** | Teresa Torres | [The Interview Snapshot](https://www.producttalk.org/interview-snapshot/) |
| CP5 | Problem Statement không chứa giải pháp | **Lean UX Canvas — Business Problem Statement** | Jeff Gothelf, *Lean UX* | [Business Problem vs Opportunity Statements](https://jeffgothelf.com/blog/business-problem-statement-opportunity-statement/) |
| CP5–CP6 | Augment hay automate; báo nhầm hay bỏ sót; tiêu chí thành công | **People + AI Guidebook — User Needs + Defining Success** | Google PAIR | [Chương User Needs](https://pair.withgoogle.com/chapter/user-needs/) |
| CP6 | No AI / Rule / Workflow / Agent; chọn mức đơn giản nhất | **Building Effective Agents** | Anthropic | [Building effective agents](https://www.anthropic.com/research/building-effective-agents) |
| CP6 | Prediction / Judgment / Action / Outcome / Input / Feedback | **AI Canvas** | Ajay Agrawal, Joshua Gans, Avi Goldfarb, *Prediction Machines* | [HBR: A Simple Tool to Start Making Decisions with the Help of AI](https://hbr.org/2018/04/a-simple-tool-to-start-making-decisions-with-the-help-of-ai) |
| CP6 | Tiêu chí đánh giá đầu ra AI trước khi xây | **AI evals cho product manager** | Hamel Husain, Shreya Shankar (Lenny's Newsletter) | [Advanced evals](https://www.lennysnewsletter.com/p/advanced-evals-how-to-find-and-fix) |
| CP6 | Quyết định theo Value / Usability / Feasibility / Viability | **Four Big Risks** | Marty Cagan, SVPG, *Inspired* | [The Four Big Risks](https://www.svpg.com/four-big-risks/) |
| CP5–CP6 | Boundary, người kiểm tra, phương án quay về | **Guidelines for Human-AI Interaction** (18 nguyên tắc) | Microsoft Research, CHI 2019 | [Guidelines for Human-AI Interaction](https://www.microsoft.com/en-us/research/publication/guidelines-for-human-ai-interaction/) |
| CP6 | Ghi rõ mục đích, bối cảnh, bên bị ảnh hưởng | **NIST AI RMF — chức năng MAP** | NIST (Mỹ) | [AI RMF Playbook: MAP](https://airc.nist.gov/airmf-resources/playbook/map/) |

## Tóm tắt từng framework (đọc 1 phút)

**Double Diamond.** Hai hình thoi nối tiếp: thoi thứ nhất là *hiểu đúng vấn đề* (Discover → Define), thoi thứ hai là *làm đúng giải pháp* (Develop → Deliver). Mỗi thoi mở rộng trước, thu hẹp sau. Lab hôm nay chỉ làm thoi thứ nhất.

**Job Story.** Thay "Là [persona], tôi muốn [tính năng]" bằng "Khi [tình huống], tôi muốn [động cơ], để [kết quả]". Tập trung vào tình huống và động cơ, không vào chân dung người dùng hay tính năng.

**Opportunity Solution Tree.** Gốc là 1 outcome đo được. Tầng giữa là opportunity: nhu cầu, pain, mong muốn của người dùng. Tầng dưới mới là solution, rồi đến thí nghiệm. Giữ hai tầng tách biệt giúp không nhảy thẳng vào giải pháp.

**Assumptions Mapping.** Viết ra mọi giả định, xếp theo *mức quan trọng* và *mức bằng chứng đã có*. Giả định quan trọng mà ít bằng chứng là thứ phải kiểm chứng trước.

**The Mom Test.** Ba luật: nói về cuộc sống của họ, không nói về ý tưởng của bạn; hỏi về chuyện cụ thể đã xảy ra, không hỏi giả định tương lai; nói ít, nghe nhiều. Lời khen không phải bằng chứng; cam kết mới là bằng chứng.

**Lean UX Problem Statement.** Problem Statement mô tả vấn đề, bối cảnh và tiêu chí thành công, nhưng **không chứa giải pháp**, để team còn không gian thử nhiều hướng.

**Google PAIR — User Needs + Defining Success.** AI không mang lại giá trị riêng cho người dùng thì dù tốt đến đâu cũng thất bại. Phải hỏi: người dùng muốn được hỗ trợ hay giao hẳn việc; nên tối ưu tránh báo nhầm hay tránh bỏ sót; ngưỡng thành công đo được là gì.

**Anthropic — Building Effective Agents.** Workflow là hệ thống mà LLM và công cụ được điều phối qua các bước định sẵn bằng code. Agent là khi LLM tự quyết quy trình và cách dùng công cụ. Nên bắt đầu từ giải pháp đơn giản nhất và chỉ thêm độ phức tạp khi cần.

**AI Canvas.** Tách một quyết định thành phần máy dự đoán (Prediction) và phần người cân nhắc (Judgment), cùng hành động, kết quả và ba loại dữ liệu: huấn luyện, đầu vào, phản hồi. Ở lab này dùng bản rút gọn, bỏ phần dữ liệu huấn luyện.

**AI evals.** Với sản phẩm AI, tiêu chí "đầu ra thế nào là đạt" là một phần của đặc tả sản phẩm, và PM là người hiểu rõ nhất "đạt" nghĩa là gì với người dùng.

**Four Big Risks.** Mọi ý tưởng sản phẩm phải vượt 4 rủi ro: Value (người dùng có muốn), Usability (có dùng được), Feasibility (có làm được), Viability (có hợp với doanh nghiệp: chi phí, pháp lý, vận hành).

**Microsoft HAX.** 18 nguyên tắc thiết kế tương tác người–AI. Bốn nguyên tắc gần nhất với lab: cho người dùng biết AI làm được gì; cho biết AI làm tốt đến mức nào; dễ sửa khi AI sai; dễ bỏ qua hoặc tắt AI.

**NIST AI RMF — MAP.** Trước khi xây hoặc mua một hệ thống AI, ghi rõ mục đích dự định, bối cảnh triển khai, người dùng, các bên bị ảnh hưởng, giả định và giới hạn.
