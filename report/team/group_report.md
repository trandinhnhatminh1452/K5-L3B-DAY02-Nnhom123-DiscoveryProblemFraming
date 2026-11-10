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
| 1 | Minh | Khi kiểm thử sự kiện hàng tháng, tôi muốn tra cứu bug cũ để tránh bỏ sót lỗi tương tự. | QA Tester phụ trách kiểm thử sự kiện | Tìm kiếm và đối chiếu bug cũ. Chưa có số liệu đo riêng; tổng thời gian kiểm thử toàn bộ sự kiện khoảng 3–4 tiếng.  | Có chắc chắn bug cũ sẽ lặp lại ở phiên bản mới không? (Dung)|
| 2 | Minh | Khi phát hiện bug không xuất hiện ổn định, tôi muốn xác định điều kiện tái hiện để không phải thử đi thử lại nhiều lần. | QA Tester phát hiện và xác minh bug; Developer hỗ trợ phân tích. |  Thay đổi điều kiện kiểm thử. Một số bug khó tái hiện có thể mất 40 phút.  | Việc tái hiện phụ thuộc vào môi trường hay data? (Dung)  |
| 3 | Minh | Khi Developer thông báo sửa bug, tôi muốn biết rõ nội dung và phạm vi sửa để xác định các trường hợp cần retest. | QA Tester thực hiện retest; Developer phụ trách sửa bug. | Làm rõ nội dung và phạm vi sửa lỗi. Theo thông tin ban đầu, mỗi lần retest có khoảng 2–3 trường hợp phải hỏi lại Developer, mất khoảng 15-20 phút xác nhận. | Có cần thiết lập rule tự động mapping giữa bug và commit code không? (Dung) |
| 4 | Dung | Khi kiểm tra một checklist dài, tôi muốn biết chính xác những mục đã kiểm tra và chưa kiểm tra, để tránh mất thời gian rà soát lại nhiều lần. | QA Tester | Mất thêm 10-15 phút rà soát trạng thái trước khi kết thúc kiểm thử | Dùng công cụ checklist thông thường có giải quyết được không? (Minh) |
| 5 | Dung | Khi nhận một tính năng mới để kiểm thử, tôi muốn nắm được các yêu cầu và thay đổi so với phiên bản trước, để xác định chính xác phạm vi cần kiểm thử. | QA Tester, Developer | Mất khoảng 15-20 phút đọc nhiều nguồn thông tin (tài liệu, ticket, trao đổi nhóm) | Thông tin phân tán ở nhiều nơi, AI đọc có bị sót ngữ cảnh không? (Minh) |


### 2.2. Cluster

| Cluster | Các candidate | Pattern chung |
|---|---|---|
| **A | Tra cứu & Khám phá thông tin cũ** | Candidate #1 (Tra cứu bug cũ khi test sự kiện), Candidate #4 (Kiểm tra checklist/trạng thái test) | Đều liên quan đến việc rà soát, tìm kiếm lại thông tin/dữ liệu đã có từ trước (bug lịch sử, danh sách mục đã test). |
| **B | Tái hiện & Phân tích lỗi** | Candidate #2 (Xác định điều kiện tái hiện bug ngẫu nhiên) | Liên quan đến việc xử lý các bài toán kỹ thuật phức tạp, tìm kiếm nguyên nhân, dấu vết (log) và điều kiện xảy ra lỗi thực tế. |
| **C | Đồng bộ thông tin & Giao tiếp nhóm** | Candidate #3 (Xác định phạm vi sửa bug của Developer), Candidate #5 (Nắm bắt yêu cầu/thay đổi tính năng mới) | Đều xuất phát từ việc thông tin phân tán hoặc thiếu đồng bộ giữa QA và Developer, dẫn đến mất thời gian xác nhận. |

### 2.3. Opportunity Solution Tree rút gọn

Gốc là **1 outcome**. Nhánh là **opportunity** (nhu cầu, pain), không phải tính năng hay công cụ.

```text
OUTCOME: Giảm thời gian QA dành cho việc thử sai và xác định điều kiện tái hiện lỗi ngẫu nhiên
├── Opportunity A: Điều kiện xảy ra bug ngẫu nhiên quá phức tạp và thiếu công cụ ghi nhận/phân tích log tự động (CHỌN)
├── Opportunity B: Thông tin lỗi cũ và checklist trạng thái nằm rời rạc, khó tra cứu nhanh
└── Opportunity C: Thiếu sự đồng bộ tức thời về phạm vi sửa lỗi và thay đổi yêu cầu giữa Dev và QA
     

Những ý đã gạch bỏ vì là solution đội lốt opportunity:
    "Công cụ tự động chạy mọi trường hợp test"    ← Solution, gạch khỏi tầng này
     "Chatbot AI tự sửa bug cho Developer"          ← Solution, gạch khỏi tầng này

```text

```
### 2.4. Chấm điểm shortlist (1–5)

| Candidate | Actor rõ | Quy trình rõ | Pain có bằng chứng | Impact đo được | Vừa sức lab | So sánh được No AI/Rule/Workflow/Agent | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| **Candidate #2 (Tái hiện bug ngẫu nhiên)** | 5 | 4 | 5 | 4 | 4 | 5 | 5 | **32** |
| **Candidate #3 (Phạm vi sửa bug của Dev)** | 5 | 4 | 4 | 4 | 5 | 4 | 5 | 31 |
| **Candidate #1 (Tra cứu bug cũ khi test sự kiện)** | 4 | 4 | 4 | 4 | 4 | 4 | 5 | 29 |

**Candidate được chọn:** Candidate #2 (Khi phát hiện bug xuất hiện trong điều kiện ngẫu nhiên/không ổn định, tôi muốn xác định chính xác điều kiện tái hiện lỗi, để không phải thử đi thử lại nhiều lần).

**Vì sao chọn:** 
- Đây là pain point gây tốn thời gian và bức bối nhất cho QA/Dev (mất 15–40 phút/lần thử sai ngẫu nhiên).
- Bài toán phân tích log, các biến môi trường và thao tác người dùng để tìm pattern lỗi rất phù hợp để so sánh rõ giữa Rule (lọc điều kiện cứng) và Workflow/AI (phân tích ngữ cảnh ngẫu nhiên), cực kỳ vừa sức trong thời lượng buổi lab.

**Vì sao loại các candidate còn lại:** 
- **Candidate #1:** Tần suất lặp lại thưa (1-2 tháng/lần), khó đo lường và kiểm chứng ngay hiệu quả trong thời gian ngắn.
- **Candidate #3:** Tác động chủ yếu nằm ở khâu giao tiếp/quy trình giữa Dev và QA, mức độ can thiệp thiên nhiều về No AI hoặc Rule đơn giản (dùng form/checklist), ít thể hiện được độ phức tạp cần xử lý.

**Xử lý bất đồng (nếu có):** Minh lo ngại Candidate #2 khó thực hiện do điều kiện ngẫu nhiên quá rộng. Nhóm đã thống nhất khoanh vùng bài toán: tập trung vào việc **gom log thao tác + phân tích sự biến đổi của các tham số**, từ đó gợi ý 2–3 kịch bản tái hiện nghi vấn nhất để QA thử nghiệm thay vì cố gắng tự động hóa toàn bộ.

---

## 3. Kiểm chứng + research giải pháp đã me (CP4)

### 3.1. Assumption Map

| # | Giả định | Loại (Value / Usability / Feasibility / Viability) | Quan trọng (1–5) | Đã có bằng chứng (1–5) | Kiểm chứng trước? |
|---:|---|---|---:|---:|---|
| 1 | QA Tester và Developer thật sự gặp khó khăn và tốn trên 20 phút cho mỗi lần thử sai khi tái hiện bug ngẫu nhiên. | Value | 5 | 4 | ✅ |
| 2 | Các yếu tố/tham số gây ra bug ngẫu nhiên (dữ liệu đầu vào, chuỗi thao tác, biến môi trường, log) có thể thu thập và ghi nhận lại được. | Feasibility | 5 | 2 | ✅ |
| 3 | QA và Dev chấp nhận tin tưởng và thử nghiệm các kịch bản tái hiện do hệ thống/AI gợi ý thay vì tự tìm kiếm thủ công. | Usability | 4 | 2 | ✅ |
| 4 | Thuật toán/AI có thể phát hiện đúng pattern (quy luật) xuất hiện lỗi từ tập dữ liệu log và tham số đầu vào. | Feasibility | 5 | 1 | ✅ |
| 5 | Ban quản lý và đội ngũ bảo mật cho phép trích xuất log thao tác và dữ liệu kiểm thử để đưa vào công cụ phân tích. | Viability | 4 | 3 | — |

*Điền 5 giả định quan trọng nhất.*

Giả định nhóm kiểm chứng trong buổi này:
- **Giả định #1 & #2:** Xác nhận thực tế thời gian lãng phí cho việc tái hiện bug ngẫu nhiên và khả năng gom dữ liệu/log tham số để phân tích.
- **Giả định #4:** Kiểm chứng tính khả thi của việc dùng Rule/AI phân tích log để đưa ra gợi ý kịch bản tái hiện chuẩn xác.

### 3.2. Kiểm chứng

Cách đã dùng: Phỏng vấn nhanh (The Mom Test) + Tra cứu thực tế từ Jira log & thảo luận cộng đồng QA.

Interview snapshot:

| Trường | Nội dung |
|---|---|
| Người được hỏi (vai trò, không ghi tên thật) | Senior QA Tester (Game/Web Project, 2 năm kinh nghiệm) |
| Câu nói đáng nhớ nhất (nguyên văn) | *"Bức bối nhất là bug ngẫu nhiên, Dev cứ bảo 'Bên máy tôi không sao' (Works on my machine) làm mình phải ngồi mò từng biến môi trường mất cả buổi."* |
| Lần gần nhất gặp vấn đề này: chuyện gì đã xảy ra? | Trong đợt kiểm thử tính năng mua hàng (In-App Purchase), bug bị văng app chỉ xuất hiện khoảng 1/10 lần thử. Phải thử lại hơn 15 lần và đổi 3 thiết bị mới xác định được lỗi do mạng yếu kết hợp với bộ nhớ RAM đầy. |
| Hiện đang xử lý bằng cách nào (workaround)? | Làm thủ công: vừa bấm vừa quay màn hình, tự mở file log đọc từng dòng, đổi từng thiết bị hoặc xóa cache ứng dụng để thử lại nhiều lần. |
| Mất bao lâu, bao lần? | Tốn khoảng 30–45 phút cho mỗi bug ngẫu nhiên; trung bình 1–2 lần/tuần. |
| Insight / opportunity rút ra | QA tốn nhiều thời gian nhất ở bước **thử sai các biến môi trường**. Nếu có công cụ tự gom log thao tác và phát hiện các biến đổi bất thường, QA chỉ cần kiểm tra 2-3 kịch bản nghi vấn thay vì mò mẫm từ đầu. |

Tổng hợp:

| Nguồn | Số người / số mẫu | Tín hiệu xác nhận | Tín hiệu phản bác |
|---|---:|---|---|
| Phỏng vấn ngắn (QA/Dev) | 2 | 2/2 người xác nhận bug ngẫu nhiên tốn thời gian nhất (trung bình 30-45p/lỗi); 100% phải quay màn hình hoặc soi log tay. | 1 người cho rằng bug do phần cứng thiết bị quá sâu thì AI/Rule cũng không bắt được logic. |
| Tra cứu Ticket Jira/Log dự án cũ | 5 ticket bug ngẫu nhiên | 4/5 ticket thiếu thông tin bước tái hiện cụ thể lúc mới mở ticket, phải comment qua lại 3-4 lần giữa QA và Dev. | 1 ticket là do lỗi mạng chập chờn từ nhà cung cấp dịch vụ (dữ liệu ngoài hệ thống). |

**Nhóm đã sửa problem thế nào sau kiểm chứng:**
- **Thu hẹp phạm vi:** Không cố gắng giải quyết bài toán "tự động tái hiện mọi loại bug" (vì quá rộng và phụ thuộc phần cứng).
- **Tập trung vào khâu nghẽn cốt lõi:** Chuyển thành bài toán **"Tự động tổng hợp chuỗi thao tác/log biến môi trường và đề xuất 2–3 kịch bản tái hiện nghi vấn nhất cho QA kiểm thử"**.

### 3.3. Research giải pháp đã có

| Công cụ / case / pattern | Link | Giải bước nào trong quy trình? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
|---|---|---|---|---|---|
| **Jam.dev / Flonnect (Developer Bug Capture)** | https://jam.dev/ | **Bước 1 & 2:** Tự động ghi nhận console log, network request, thiết bị, và thao tác màn hình ngay khi QA thấy lỗi. | Gom tự động 100% dữ liệu kỹ thuật và biến môi trường; tạo ticket kèm bằng chứng chi tiết chỉ bằng 1-click. | Chỉ ghi nhận được dữ liệu phiên chạy hiện tại (front-end/browser), không tự phân tích so sánh để tìm nguyên nhân gốc của tính ngẫu nhiên. | Rút ngắn khâu thu thập log; dữ liệu log cần được cấu trúc hóa để làm đầu vào cho bước phân tích pattern tiếp theo. |
| **Sentry / Rollbar (Error Monitoring & Log Analysis)** | https://sentry.io/ | **Bước 2 & 3:** Phân tích stack trace, theo dõi tần suất lỗi ngẫu nhiên và nhóm (group) các lỗi có cùng nguyên nhân gốc. | Tự động phân loại lỗi ngẫu nhiên, chỉ ra chính xác dòng code và tham số gây crash trên backend/system. | Chi phí cao, lượng log khổng lồ dễ gây "nhiễu" (log noise); khó sử dụng cho QA nếu không có kỹ năng đọc sâu log code. | Cần cơ chế lọc (filter) để chỉ giữ lại các tham số thay đổi cốt lõi, tránh gây quá tải thông tin cho QA. |
| **Pattern: Reproduction Test Builder (Prompt / Script)** | Case study: AI Pattern Book - Reproduction Test | **Bước 3 & 4:** Đưa log thao tác + biến môi trường vào prompt/script để gợi ý kịch bản tái hiện tối giản. | Đưa ra các bước nghi vấn cực kỳ cụ thể (1-2-3); giúp QA không phải thử lại 15–20 trường hợp ngẫu nhiên. | Nếu dữ liệu log đầu vào thiếu hoặc sai, AI sẽ gợi ý các bước tái hiện sai lệch (hallucination). | Áp dụng mô hình **Workflow**: dùng Rule/Script gom log chuẩn trước, sau đó mới dùng AI tóm tắt thành 2–3 kịch bản tái hiện cho QA duyệt và thử. |

---

## 4. Quy trình trước/sau (CP5)

### 4.1. Quy trình hiện tại

| Bước | Actor | Input | Output | Thời gian / tần suất | Ghi chú |
|---:|---|---|---|---|---|
| 1 | QA Tester | Thao tác kiểm thử trên ứng dụng/game | Phát hiện bug xuất hiện không ổn định (ngẫu nhiên) | 5 phút / Mỗi khi gặp lỗi ngẫu nhiên | Lỗi chỉ xuất hiện 1/5 hoặc 1/10 lần thử. |
| 2 | QA Tester | Phiên chạy ứng dụng vừa bị lỗi | File log thô, video/ảnh màn hình thao tác | 10 phút / Mỗi lần gặp bug | Phải mở nhiều công cụ (Console, Network Tab, Screen Recorder) để lấy log. |
| 3 | QA Tester | File log thô, nghi vấn ban đầu | Danh sách các lần thử thất bại/thành công | **20 phút** / Mỗi lần gặp bug | **BOTTLENECK:** Phải liên tục thay đổi cấu hình thiết bị, xóa cache, đổi tài khoản, đổi mạng để dò tìm điều kiện. |
| 4 | QA Tester | Kết quả sau nhiều lần thử sai | Các bước tái hiện (Reproduction Steps) nghi vấn | 7 phút / Mỗi lần gặp bug | Viết lại các bước vào nháp, đôi khi vẫn thiếu điều kiện ngầm (vd: RAM đầy). |
| 5 | QA Tester | Các bước tái hiện nháp | Ticket bug trên Jira / Redmine | 3 phút / Mỗi lần gặp bug | Gửi ticket cho Developer để chờ xử lý. |


**Bottleneck chính:**

---

### 4.2. Quy trình tương lai

| Bước | Actor | Input | Output | Thời gian | Ghi chú / Mức can thiệp |
|---:|---|---|---|---|---|
| 1 | Hệ thống / Script | Phiên chạy ứng dụng bị lỗi | Gói dữ liệu log thô, network request, trạng thái thiết bị | 2 phút | **Rule/Script:** Tự động gom log và biến môi trường ngay khi gặp lỗi (tương tự công cụ Jam). |
| 2 | Hệ thống AI | Gói dữ liệu log và tham số | Danh sách 2–3 kịch bản tái hiện nghi vấn nhất | 2 phút | **AI (Workflow):** Phân tích pattern, so sánh sự thay đổi tham số để khoanh vùng nguyên nhân. |
| 3 | QA Tester | Kịch bản tái hiện từ hệ thống | Kết quả xác thực kịch bản đúng/sai | 8 phút | **Con người:** QA trực tiếp chạy thử kịch bản tối ưu thay vì mò mẫm từ đầu. |
| 4 | Hệ thống | Kết quả xác thực của QA | Ticket bug hoàn chỉnh trên Jira | 3 phút | **Rule:** Tự động đính kèm log và các bước tái hiện chuẩn vào ticket. |


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
