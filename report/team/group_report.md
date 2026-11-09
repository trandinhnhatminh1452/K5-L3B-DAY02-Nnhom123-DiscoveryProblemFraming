# Báo cáo nhóm — Day 02 Discovery & Problem Framing

> Bản chung của nhóm, viết trên repo do nhóm trưởng fork. Không copy file này sang repo cá nhân.
> Template chi tiết và prompt mẫu: [docs/01-worksheet.md](../../docs/01-worksheet.md). Bài mẫu: [docs/02-deliverable-example.md](../../docs/02-deliverable-example.md).

## 1. Thông tin nhóm

- Tên nhóm: Nnhom123
- Thành viên: xem `TEAM.md`
- Candidate problem được chọn (1 câu):
- Quyết định cuối: Go / Not Yet / No-Go

---

## 2. Hội tụ nhóm (CP3)

### 2.1. Pitch

| # | Người đưa ra | Candidate (Job Story ngắn) | Actor | Bottleneck | Câu hỏi phản biện nhận được (ai hỏi) |
|---:|---|---|---|---|---|
| 1 | Tôi | Khi kiểm thử sự kiện hàng tháng, tôi muốn tra cứu bug cũ để tránh bỏ sót lỗi tương tự. | QA Tester phụ trách kiểm thử sự kiện | Tìm kiếm và đối chiếu bug cũ. Chưa có số liệu đo riêng; tổng thời gian kiểm thử toàn bộ sự kiện khoảng 3–4 tiếng.  | Có chắc chắn bug cũ sẽ lặp lại ở phiên bản mới không? (Dung)|
| 2 | Tôi | Khi phát hiện bug không xuất hiện ổn định, tôi muốn xác định điều kiện tái hiện để không phải thử đi thử lại nhiều lần. | QA Tester phát hiện và xác minh bug; Developer hỗ trợ phân tích. |  Thay đổi điều kiện kiểm thử. Một số bug khó tái hiện có thể mất 40 phút.  | Việc tái hiện phụ thuộc vào môi trường hay data? (Dung)  |
| 3 | Tôi | Khi Developer thông báo sửa bug, tôi muốn biết rõ nội dung và phạm vi sửa để xác định các trường hợp cần retest. | QA Tester thực hiện retest; Developer phụ trách sửa bug. | Làm rõ nội dung và phạm vi sửa lỗi. Theo thông tin ban đầu, mỗi lần retest có khoảng 2–3 trường hợp phải hỏi lại Developer, mất khoảng 15-20 phút xác nhận. | Có cần thiết lập rule tự động mapping giữa bug và commit code không? (Dung) |
| 4 | Dung | Khi kiểm tra một checklist dài, tôi muốn biết chính xác những mục đã kiểm tra và chưa kiểm tra, để tránh mất thời gian rà soát lại nhiều lần. | QA Tester | Mất thêm 10-15 phút rà soát trạng thái trước khi kết thúc kiểm thử | Dùng công cụ checklist thông thường có giải quyết được không? (Minh) |
| 5 | Dung | Khi nhận một tính năng mới để kiểm thử, tôi muốn nắm được các yêu cầu và thay đổi so với phiên bản trước, để xác định chính xác phạm vi cần kiểm thử. | QA Tester, Developer | Mất khoảng 15-20 phút đọc nhiều nguồn thông tin (tài liệu, ticket, trao đổi nhóm) | Thông tin phân tán ở nhiều nơi, AI đọc có bị sót ngữ cảnh không? (Minh) |


### 2.2. Cluster

| Cluster | Các candidate | Pattern chung |
|---|---|---|
| A | | |
| B | | |
| C | | |

### 2.3. Opportunity Solution Tree rút gọn

Gốc là **1 outcome**. Nhánh là **opportunity** (nhu cầu, pain), không phải tính năng hay công cụ.

```text
OUTCOME: 
├── Opportunity A: 
├── Opportunity B: 
└── Opportunity C: 
```

Những ý đã gạch bỏ vì là solution đội lốt opportunity:

-

### 2.4. Chấm điểm shortlist (1–5)

| Candidate | Actor rõ | Quy trình rõ | Pain có bằng chứng | Impact đo được | Vừa sức lab | So sánh được No AI/Rule/Workflow/Agent | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| | | | | | | | | |
| | | | | | | | | |
| | | | | | | | | |

**Candidate được chọn:**

**Vì sao chọn:**

**Vì sao loại các candidate còn lại:**

**Xử lý bất đồng (nếu có):**

---

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
| **Actor** | QA Tester trực tiếp kiểm thử chức năng game, phát hiện và xác minh các bug không xuất hiện ổn định. Developer hỗ trợ phân tích khi cần. |
| **Quy trình** | 1. Thực hiện thao tác kiểm thử.<br>2. Phát hiện bug.<br>3. Thử thực hiện lại các thao tác trước đó.<br>4. Thay đổi điều kiện kiểm thử như trạng thái game, thao tác, thời điểm hoặc dữ liệu.<br>5. Ghi nhận kết quả từng lần thử.<br>6. Báo cáo bug nếu tái hiện được. |
| **Bottleneck** | Bước 4: Thay đổi điều kiện kiểm thử. Một số bug khó tái hiện có thể mất 40 phút.  |
| **Impact** | Tốn thời gian kiểm thử, làm chậm quá trình xác minh và báo cáo bug. Nếu không tái hiện được, QA có thể không cung cấp đủ thông tin để Developer xác định nguyên nhân và sửa lỗi. |
| **Success Metric** (baseline → target, cách đo) |  Giảm 30% thời gian trung bình để tái hiện một bug. Ghi lại thời gian từ lúc bắt đầu xác minh bug đến khi tái hiện thành công hoặc kết thúc quá trình thử; so sánh trước và sau pilot trên các bug tương tự. |
| **Boundary** (AI không được làm gì; khi nào cần con người kiểm tra — HITL) |AI Không tự kết luận nguyên nhân bug khi chưa đủ bằng chứng; không tự thay đổi dữ liệu hoặc trạng thái game; không tự đóng ticket hoặc xác nhận bug đã được sửa. QA phải kiểm tra và xác nhận các điều kiện tái hiện được đề xuất trước khi báo cáo Developer. |

Phản biện nhận được (từ AI hoặc nhóm khác) và nhóm có đồng ý không:

1. **Bottleneck:** Chưa xác định rõ nguyên nhân khiến QA mất nhiều thời gian: thiếu thông tin, thiếu phương pháp kiểm thử hay phải thực hiện quá nhiều thao tác.

2. **Metric:** Chưa có baseline đáng tin cậy và chưa xác định cách tính thời gian đối với những bug không tái hiện thành công.

3. **Boundary:** Chưa xác định rõ phạm vi công việc AI được phép thực hiện và mức độ can thiệp của AI vào quy trình kiểm thử.

Nhóm đồng ý và ưu tiên kiểm chứng ba điểm này bằng dữ liệu và phỏng vấn QA thực tế, thay vì vội vàng thiết kế chức năng AI.
---

## 6. Mức can thiệp AI (CP6)

### 6.1. Ma trận độ mơ hồ × độ phức tạp

**Độ mơ hồ cao**: Chưa xác định rõ nguyên nhân khiến bug xuất hiện không ổn định. Điều kiện tái hiện bug cũng chưa được xác định rõ.


**Độ phức tạp trung bình**: Quy trình hiện tại gồm nhiều bước thử lại thao tác, thay đổi điều kiện và ghi nhận kết quả. Tuy nhiên, đây vẫn là quy trình kiểm thử có phạm vi tương đối rõ ràng, chưa đòi hỏi xử lý một hệ thống quá phức tạp.

### 6.2. So sánh 4 mức

| Mức | Phương án cho bài của nhóm | Đủ khi nào | Rủi ro | Chọn? |
|---|---|---|---|---|
| **No AI**  | Chuẩn hóa checklist ghi nhận thao tác, trạng thái game, dữ liệu, thời điểm và kết quả mỗi lần thử. | QA có thể dựa vào thông tin đã ghi nhận để tái hiện bug mà không phải thử lại quá nhiều lần. | QA phải ghi chép thủ công; dễ thiếu thông tin hoặc ghi nhận không nhất quán. | Có thể thử|
| **Rule** | Xây dựng các quy tắc dựa trên lịch sử kiểm thử để gợi ý những điều kiện cần thử khi bug xuất hiện. | Các điều kiện gây lỗi có quy luật tương đối rõ và có thể mô tả bằng các quy tắc cụ thể. | Không xử lý tốt những bug có điều kiện phức tạp hoặc chưa từng xuất hiện. | Có thể thử |
| **Workflow** | Xây dựng quy trình hỗ trợ QA: ghi nhận thông tin bug, tổng hợp lịch sử thử nghiệm và đề xuất các bước kiểm tra tiếp theo. | Các bước xử lý có thể chuẩn hóa và việc tổng hợp thông tin giúp QA tiết kiệm thời gian. | Quy trình có thể trở nên rườm rà; đề xuất không phù hợp nếu dữ liệu đầu vào thiếu. | Chọn |
| **Agent** | Xây dựng AI Agent phân tích log và lịch sử thử nghiệm, đề xuất điều kiện hoặc tổ hợp thao tác có khả năng tái hiện bug. | Có đủ dữ liệu log và lịch sử kiểm thử chất lượng để Agent phân tích, đồng thời kết quả đề xuất tốt hơn phương pháp đơn giản. | Đề xuất sai hoặc thiếu căn cứ; khó kiểm soát nếu Agent tự thực hiện thao tác hoặc thay đổi trạng thái game. | Không chọn |

**Mức chọn:** Workflow

**Vì sao không chọn mức đơn giản hơn:** No AI chỉ chuẩn hóa việc ghi nhận thông tin, chưa hỗ trợ phân tích lịch sử và đề xuất bước kiểm tra tiếp theo. Rule thiếu linh hoạt với các bug có điều kiện tái hiện phức tạp. Workflow giúp tổng hợp thông tin và hướng dẫn QA kiểm tra có hệ thống, đồng thời vẫn để QA quyết định.

### 6.3. AI Canvas rút gọn

| Thành phần | Nội dung |
|---|---|
| **Prediction** — AI dự đoán / tạo ra gì? | Tổng hợp lịch sử kiểm thử và đề xuất các điều kiện, thao tác tiếp theo có khả năng tái hiện bug. |
| **Judgment** — con người cân nhắc, quyết định gì? | QA đánh giá đề xuất có phù hợp không và lựa chọn điều kiện cần thử. |
| **Action** — hành động cuối cùng là gì, ai làm? | QA thực hiện kiểm thử theo các điều kiện đã chọn và ghi nhận kết quả. |
| **Outcome** — đo kết quả bằng gì? | Thời gian trung bình để tái hiện bug và tỷ lệ bug tái hiện thành công. |
| **Input** — AI cần dữ liệu đầu vào gì mỗi lần chạy? Có sẵn không? | Mô tả bug, thao tác kiểm thử, trạng thái game, dữ liệu và lịch sử thử nghiệm. Hiện có thể ghi nhận một phần, cần kiểm tra mức độ đầy đủ. |
| **Feedback** — lấy phản hồi ở đâu để cải thiện? | Kết quả thực tế sau mỗi lần thử: tái hiện thành công hay thất bại, điều kiện nào hiệu quả và đánh giá của QA. |

### 6.4. Hai câu hỏi của Google PAIR

- Người dùng muốn **được hỗ trợ (augment)**: AI chỉ đóng vai trò tổng hợp lịch sử kiểm thử và đề xuất các điều kiện có khả năng tái hiện bug. QA vẫn là người đánh giá, lựa chọn và trực tiếp thực hiện kiểm thử.
- AI sai kiểu **bỏ sót** tệ hơn: Bỏ sót lỗi khiến developer không thể khắc phục sẽ gây ảnh hưởng trải nghiệm chơi của khách hànghàng. Vì vậy không được bỏ sót các lỗi có thể xảy ra

---

## 7. Problem Statement v1 + tiêu chí đánh giá (CP6)

| Trường | Nội dung |
|---|---|
| **Actor** | QA Tester trực tiếp kiểm thử chức năng game, phát hiện và xác minh các bug không xuất hiện ổn định. Developer hỗ trợ phân tích khi cần. |
| **Quy trình** | 1. Thực hiện thao tác kiểm thử.<br>2. Phát hiện bug.<br>3. Thử thực hiện lại các thao tác trước đó.<br>4. Thay đổi điều kiện kiểm thử như trạng thái game, thao tác, thời điểm hoặc dữ liệu.<br>5. Ghi nhận kết quả từng lần thử.<br>6. Báo cáo bug nếu tái hiện được. |
| **Bottleneck** | Bước 4: Thay đổi điều kiện kiểm thử. Một số bug khó tái hiện có thể mất 40 phút.  |
| **Impact** | Tốn thời gian kiểm thử, làm chậm quá trình xác minh và báo cáo bug. Nếu không tái hiện được, QA có thể không cung cấp đủ thông tin để Developer xác định nguyên nhân và sửa lỗi. |
| **Success Metric** (baseline → target, cách đo) |  Giảm 30% thời gian trung bình để tái hiện một bug. Ghi lại thời gian từ lúc bắt đầu xác minh bug đến khi tái hiện thành công hoặc kết thúc quá trình thử; so sánh trước và sau pilot trên các bug tương tự. |
| **Boundary** (AI không được làm gì; khi nào cần con người kiểm tra — HITL) |AI Không tự kết luận nguyên nhân bug khi chưa đủ bằng chứng; không tự thay đổi dữ liệu hoặc trạng thái game; không tự đóng ticket hoặc xác nhận bug đã được sửa. QA phải kiểm tra và xác nhận các điều kiện tái hiện được đề xuất trước khi báo cáo Developer. |
| **AI intervention point** | Sau khi QA ghi nhận bug và kết quả các lần thử, AI tổng hợp lịch sử kiểm thử, đề xuất điều kiện và bước kiểm tra tiếp theo. |
| **Mức chọn** | **Workflow** |
| **Rủi ro & người kiểm tra** | AI có thể đề xuất điều kiện không phù hợp hoặc bỏ sót điều kiện gây lỗi. QA kiểm tra căn cứ, lựa chọn đề xuất và xác nhận bằng kiểm thử thực tế. |
**Thay đổi so với v0 và lý do:**

| Trường | v0 | v1 | Vì sao đổi |
|---|---|---|---|
| Quy trình | Chưa mô tả rõ vai trò AI trong quy trình. | Bổ sung bước AI tổng hợp lịch sử và đề xuất bước kiểm tra tiếp theo. | Xác định rõ vị trí AI hỗ trợ QA. |
| Rủi ro & người kiểm tra | Chưa nêu rõ rủi ro AI đề xuất sai hoặc bỏ sót. | Bổ sung rủi ro và trách nhiệm kiểm tra của QA. | Đảm bảo độ tin cậy của kết quả. |

**Tiêu chí đánh giá đầu ra của AI (3–5 tiêu chí):**

| # | Tiêu chí | Đạt khi | Không đạt khi |
|---:|---|---|---|
| 1 | Tính liên quan | Điều kiện AI đề xuất liên quan đến mô tả bug và lịch sử kiểm thử. | Đề xuất không liên quan đến bug. |
| 2 | Tính cụ thể | Đề xuất rõ thao tác, trạng thái game và dữ liệu cần kiểm tra. | Chỉ đưa ra gợi ý chung chung, khó thực hiện. |
| 3 | Tính có căn cứ | Có thông tin từ lịch sử thử nghiệm hoặc log làm căn cứ cho đề xuất. | Đưa ra đề xuất không có bằng chứng hỗ trợ. |
| 4 | Khả năng tái hiện | Điều kiện được đề xuất giúp QA tái hiện bug trong kiểm thử thực tế. | Thử theo đề xuất nhưng không tái hiện được bug. |
| 5 | Tính an toàn | AI chỉ đề xuất, không tự thay đổi trạng thái game hoặc kết luận bug. | AI tự thực hiện hành động hoặc đưa ra kết luận thay QA. |

---

## 8. Quyết định (CP6)

### 8.1. Bốn rủi ro

| **Rủi ro** | **Mức độ rủi ro (Thấp = an toàn)** | **Lý do / bằng chứng** |
|---|---|---|
| **Value** | Trung bình | QA có nhu cầu giảm thời gian tái hiện bug, nhưng chưa có kết quả pilot chứng minh Workflow giúp tiết kiệm thời gian thực tế. |
| **Usability** | Thấp | QA đã quen với quy trình kiểm thử và có thể đánh giá, lựa chọn hoặc bỏ qua các điều kiện AI đề xuất. |
| **Feasibility** | Cao | Chưa xác định log và lịch sử kiểm thử có đầy đủ, có cấu trúc và đủ dữ liệu để AI phân tích hay không. |
| **Viability** | Trung bình | Cần xem xét chi phí triển khai, bảo mật dữ liệu game và nguồn lực duy trì hệ thống. |

### 8.2. Kết luận

**Quyết định:**  Not Yet 

**Lý do:**  Workflow có tiềm năng hỗ trợ QA giảm thời gian tái hiện bug, nhưng chưa xác nhận được chất lượng và mức độ đầy đủ của dữ liệu log, lịch sử kiểm thử, các trường hợp test mới hay test case khó có thể khiến AI không đạt được kết quả như ý trong thời gian mong muốn 


**Nếu Not Yet — cần kiểm chứng gì trước:** 
- Kiểm tra dữ liệu log và lịch sử kiểm thử có đủ thông tin không.

- Xác nhận AI có thể đưa ra gợi ý cụ thể, hữu ích.

- Kiểm tra trên test khó và mới 

- Lấy phản hồi từ QA về tính dễ sử dụng.


**Ngưỡng dừng** (nếu sau … mà … thì quay về …):Nếu sau pilot AI không giúp giảm ít nhất 30% thời gian tái hiện bug hoặc QA thường xuyên phải bỏ qua đề xuất, quay về checklist và quy trình ghi nhận thủ công.

---

## 9. Hạn chế và hướng tiếp theo

Hạn chế:
- Chưa có số liệu thực tế đủ lớn để xác định chính xác thời gian trung bình tái hiện bug.
- Dữ liệu log và lịch sử kiểm thử có thể chưa đầy đủ hoặc thiếu cấu trúc.
- AI có thể đề xuất sai hoặc bỏ sót điều kiện tái hiện bug trên các test khó hoặc mới.
- Hiệu quả của Workflow chưa được kiểm chứng qua pilot thực tế.

Hướng tiếp theo:
- Thu thập dữ liệu từ các bug khó tái hiện trong quá trình kiểm thử.
- Chuẩn hóa checklist và template ghi nhận kết quả từng lần thử.
- Xây dựng prototype Workflow hỗ trợ tổng hợp thông tin và đề xuất điều kiện kiểm thử.
- Thử nghiệm với một nhóm QA nhỏ, đo thời gian tái hiện bug và lấy phản hồi.
- Dựa trên kết quả pilot để quyết định tiếp tục phát triển hay quay về giải pháp không dùng AI.

## 10. Tài liệu tham khảo

-
