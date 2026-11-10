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


