# Team

> Điền file này trên repo chung do nhóm trưởng fork. Nhóm điền phần **Thông tin nhóm** và **Thành viên**. Mỗi người tự điền phần của mình trong **Cá nhân**. Không copy file này sang repo khác.

## Thông tin nhóm

- Tên nhóm: Nnhom123
- Candidate problem nhóm chọn (1 câu): Khi phát hiện bug không xuất hiện ổn định, QA muốn xác định điều kiện tái hiện mà không phải thử đi thử lại nhiều lần.
- Quyết định cuối (Go / Not Yet / No-Go):  Not Yet

## Thành viên

| STT | Họ và tên | MSSV | Vai trò trong nhóm | Tài khoản GitHub |
|---:|---|---|---|---|
| 1 |Trần Đình Nhật Minh |2A202604083|Đề xuất candidate, vẽ quy trình, viết Problem Statement  |trandinhnhatminh1452 |
| 2 |Đặng Thùy Dung | 2A202604116 |Phụ trách research và kiểm chứng (phỏng vấn, tra cứu Jira), vẽ quy trình, phản biện | dungdt1410 |

Không ghi email hay số điện thoại vào bảng này, vì repo có thể để public.

Gợi ý vai trò (một người có thể giữ nhiều vai): điều phối thời gian, ghi chép, người phản biện chính, phụ trách kiểm chứng (phỏng vấn/survey), phụ trách research, vẽ quy trình, viết Problem Statement.

## Phân công theo checkpoint

| Checkpoint | Người chính | Người hỗ trợ | Sản phẩm |
|---|---|---|---|
| CP3 — Hội tụ nhóm | Dung | Minh | Cluster, cây OST, bảng chấm điểm |
| CP4 — Kiểm chứng | Dung | Minh | Assumption map, snapshot hoặc survey |
| CP4 — Research | Dung | Minh | Bảng research có link |
| CP5 — Quy trình trước/sau | Dung | Minh | Quy trình + bảng before/after |
| CP5 — Problem Statement v0 | Minh | Dung | Problem Statement v0 |
| CP6 — Mức can thiệp + Problem Statement v1 | Minh | Dung | Ma trận, AI Canvas, eval, Problem Statement v1 |
| CP6 — Quyết định | Minh | Dung | 4 rủi ro + Go/Not Yet/No-Go |

## Cá nhân

Mỗi thành viên thêm một mục theo mẫu dưới đây, tiêu đề là `HoVaTen-MSSV`.

### Trần Đình Nhật Minh - [2A202604083]

**Phần việc phụ trách:**

- Đề xuất và phân tích các vấn đề liên quan đến công việc QA Tester.
- Xây dựng Problem Card cho vấn đề bug xuất hiện không ổn định, khó tái hiện.
- Xây dựng và điều chỉnh Problem Statement v0, v1 sau khi nhận phản biện.
- Phân tích các mức can thiệp AI và đánh giá rủi ro của giải pháp.

**Đóng góp cụ thể (mình đã làm gì, ra sản phẩm gì):**

- Đề xuất 3 vấn đề trong công việc QA: tra cứu bug cũ, tái hiện bug ngẫu nhiên và xác định phạm vi sửa bug.
- Phân tích quy trình tái hiện bug, xác định bottleneck, impact và success metric.
- Điều chỉnh Problem Statement, bổ sung Boundary, AI intervention point và cách đo hiệu quả.
- So sánh 4 mức can thiệp No AI, Rule, Workflow và Agent; đề xuất chọn Workflow.
- Đánh giá 4 nhóm rủi ro Value, Usability, Feasibility và Viability, từ đó đưa ra quyết định Not Yet.

**Bằng chứng (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):**

- `group_report.md`: phần CP5 — Problem Statement v0, CP6 — Mức can thiệp + Problem Statement v1, CP6 — Quyết định 
- `report/assets/`: [Bổ sung tên file minh chứng thực tế nếu có].

**Điều mình học được từ phần nhóm:** 
Qua bài làm, tôi học được cách xác định vấn đề trước khi nghĩ đến giải pháp. Tôi nhận ra một ý tưởng sử dụng AI nghe có vẻ phù hợp nhưng vẫn cần được kiểm chứng về dữ liệu đầu vào, tính khả thi và hiệu quả thực tế. Ngoài ra, tôi hiểu rõ hơn cách xây dựng Problem Statement, xác định vai trò giữa AI và con người, cũng như lựa chọn mức can thiệp phù hợp thay vì cố gắng sử dụng AI ở mức phức tạp nhất.

### DangThuyDung-2A202604116
 
**Phần việc phụ trách:**
 
- Đề xuất và phân tích các vấn đề liên quan đến công việc QA Tester.
- Research và kiểm chứng (CP4): phỏng vấn QA, tra cứu ticket Jira, research giải pháp đã có.
- Vẽ quy trình trước/sau của việc tái hiện bug.
- Phản biện các candidate và các bản Problem Statement.
**Đóng góp cụ thể (mình đã làm gì, ra sản phẩm gì):**
 
- Đề xuất 2 vấn đề: kiểm tra checklist dài khó theo dõi mục đã/chưa kiểm tra (Candidate #4) và nắm yêu cầu, thay đổi của tính năng mới để xác định phạm vi kiểm thử (Candidate #5).
- Đặt câu hỏi phản biện cho 3 candidate của Minh: bug cũ có chắc lặp lại không (#1), việc tái hiện phụ thuộc môi trường hay dữ liệu (#2), có cần rule tự động mapping giữa bug và commit không (#3).
- Kiểm chứng vấn đề bằng phỏng vấn QA và tra cứu 5 ticket Jira bug ngẫu nhiên; tổng hợp tín hiệu xác nhận và phản bác.
- Research các giải pháp đã có (Jam, Sentry/Rollbar, Crashlytics/Instabug, pattern Reproduction Test Builder) và rút bài học cho nhóm.
- Tham gia vẽ quy trình hiện tại và quy trình tương lai.
- 
**Bằng chứng (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):**
 
- `group_report.md`: mục 2.1 (Pitch và câu hỏi phản biện), mục 3 (CP4 — Kiểm chứng + research), mục 4 (CP5 — Quy trình trước/sau).
- `report/assets/`: [Bổ sung tên file minh chứng thực tế nếu có].

**Điều mình học được từ phần nhóm:**
Mình học được cách đi từng bước để biến một ý tưởng thành quy trình vận hành cho một dự án thật: từ pitch, phân cụm, chọn vấn đề, kiểm chứng bằng phỏng vấn và dữ liệu, vẽ quy trình trước/sau, viết Problem Statement, chọn mức can thiệp AI, rồi mới đưa ra quyết định Go / Not Yet / No-Go. Mỗi bước phải có số liệu hoặc bằng chứng làm căn cứ cho bước sau, không thể nhảy thẳng đến giải pháp.

Một bài học quan trọng khác là những gì AI nói nghe có vẻ rất hợp lý và thuyết phục, nhưng vẫn phải kiểm chứng lại. Khi dùng AI góp ý cho báo cáo, nhóm phát hiện nhiều chỗ nghe thì đúng nhưng thực tế chưa có căn cứ, ví dụ các con số thời gian không thống nhất giữa các mục, giả định log có thể gom tự động chưa được thử với dữ liệu thật, hay kết luận mạnh hơn bằng chứng khi mới có 2 phỏng vấn và 5 ticket. Vì vậy, tôi rút ra rằng AI nên được dùng để gợi ý và phản biện, còn con người phải là người kiểm tra số liệu, nguồn và quyết định cuối cùng.
 


