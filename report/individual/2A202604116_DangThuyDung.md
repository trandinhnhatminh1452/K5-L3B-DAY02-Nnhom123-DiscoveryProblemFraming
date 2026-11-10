
# Báo cáo cá nhân — 2A202604116_DangThuyDung.md

> Đổi tên file theo quy tắc `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md` (MSSV trước, dấu `_`, họ tên viết liền không dấu). Sửa cả dòng tiêu đề phía trên cho khớp.
> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: copy template này thành file mới, điền, rồi commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên: Đặng Thùy Dung
- MSSV: 2A202604116
- Email trường (không bắt buộc, repo có thể để public):
- Tên nhóm: Nnhom123
- Link repo nhóm: 

---
## 2. Scan problem (CP1)

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

| # | Lăng kính | Job Story: Khi… tôi muốn… để… | Ai chịu ảnh hưởng? | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng) |
|---:|---|---|---|---|
| 1 | **Lặp lại** | Khi đến thứ Bảy hằng tuần, tôi muốn chốt lịch ca trực cho 8–10 nhân viên part-time (với lịch rảnh rỗi và mong muốn làm việc thay đổi liên tục), để không phải mất 2-3 tiếng ghép lịch thủ công và xử lý khiếu nại chồng chéo. | Quản lý ca trực, 8–10 NV part-time | Mất 150–180 phút/tuần; trung bình 2–3 cuộc xin đổi ca/khiếu nại trùng lịch mỗi tuần. |
| 2 | **Tốn thời gian** | Khi cần chốt ca trực gấp cho ngày hôm sau do có nhân viên nghỉ đột xuất, tôi muốn tìm nhanh nhân viên rảnh và đủ điều kiện ca, để không phải nhắn tin hỏi từng người. | Quản lý ca trực, NV part-time | Mất 30–45 phút nhắn tin/gọi điện hỏi từng người trong nhóm chat Zalo. |
| 3 | **Cần đọc, tổng hợp nhiều thông tin** | Khi nhân viên gửi lịch rảnh bằng nhiều hình thức (tin nhắn text, ảnh chụp thời khóa biểu, voice note), tôi muốn tự động tổng hợp thành bảng dữ liệu, để không phải nhập tay từng dòng vào Excel. | Quản lý ca trực | Mất khoảng 40–50 phút đọc lại tin nhắn và điền tay vào file Excel theo dõi. |
| 4 | **Tốn thời gian** | Khi cuối tháng tính lương, tôi muốn đối soát tổng số giờ làm thực tế của từng nhân viên với lịch đã phân công, để tránh sai sót khi phát lương. | Quản lý, Kế toán | Mất 60–90 phút mỗi cuối tháng rà soát lại sổ chấm công và bảng lịch cũ. |
| 5 | **Pain từ người khác** | Khi nhân viên tự thỏa thuận đổi ca cho nhau, tôi muốn họ cập nhật đúng quy trình, để bảng lịch chung luôn đúng mà tôi không phải làm trung gian xác nhận nhiều lần. | Quản lý ca trực, NV part-time | Mỗi tuần có 3–4 lượt đổi ca qua lại; mất 15–20 phút/lần xác nhận và sửa file. |

**Nếu có dùng AI để gợi ý thêm:** 
* *Ý AI gợi ý giữ lại:* Ý #3 (tự động tổng hợp nguyện vọng từ tin nhắn tự do) vì đây là pain thực tế khi nhân viên không điền đúng form.
* *Ý AI gợi ý bỏ:* Ý "tự động nhắn tin nhắc nhân viên đi làm đúng giờ" vì tính năng nhắn tin nhắc lịch có thể xử lý bằng Rule/bot tự động đơn giản, không cần dùng AI và không nằm ở khâu nghẽn xếp lịch.

---

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

 
### Bảng chọn top 3
 
| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 | **Tối ưu lịch làm part-time hằng tuần (#1)** | Quy trình lặp lại rõ ràng, tốn nhiều thời gian thử sai, có baseline đo đếm bằng phút cụ thể. | Làm sao để xử lý các ràng buộc phức tạp (ca gãy, giới hạn giờ/tuần) tự động? |
| 2 | **Tổng hợp lịch rảnh từ tin nhắn tự do (#3)** | Giúp giảm bớt bước nhập liệu đầu vào, giảm tải cho quản lý. | Khả năng đọc chính xác hình ảnh thời khóa biểu hoặc voice note của AI. |
| 3 | **Xử lý tìm người thay ca đột xuất (#2)** | Giải quyết pain khẩn cấp trong vận hành hằng ngày. | Nhân viên có sẵn sàng nhận ca gấp khi bot gửi thông báo không. |

### Problem Card #1

| Trường | Nội dung |
|---|---|
| Job Story | Khi đến thứ Bảy hằng tuần cần chốt lịch ca trực cho 8-10 nhân viên part-time (với lịch rảnh rỗi và mong muốn làm việc thay đổi liên tục), tôi muốn có một phương án sắp xếp ca làm tối ưu hóa nguyện vọng của nhân viên và yêu cầu vận hành, để không phải mất 2-3 tiếng ghép lịch thủ công và xử lý khiếu nại chồng chéo. |
| Actor | Quản lý cửa hàng / Trưởng nhóm phụ trách ca trực |
| Thời điểm / bối cảnh | Sáng thứ Bảy hằng tuần, trước buổi chốt lịch ca làm cho tuần tiếp theo |
| Quy trình hiện tại (3–7 bước) | 1. Thu thập lịch rảnh qua Form/Zalo (30') → 2. Nhập liệu và tổng hợp nguyện vọng vào Excel (20') → 3. Thử sai & Ghép lịch thủ công (60') → 4. Kiểm tra xung đột & sót ca (25') → 5. Công bố & Điều chỉnh theo phản hồi (15') |
| Bottleneck (bước nào, mất bao nhiêu phút) | **Bước 3: Thử sai & Ghép lịch thủ công** (mất 60 phút do rào cản chéo giữa số giờ tối đa/tuần, số người tối thiểu/ca, ca gãy, lịch học nhân viên). |
| Impact (nếu không giải thì sao) | Mất 150–180 phút/tuần; 2–3 cuộc khiếu nại/xin đổi ca mỗi tuần do xếp trùng lịch bận; nguy cơ thiếu người giờ cao điểm. |
| Success metric (baseline → target) | Baseline: **150 phút/tuần** → Target: **dưới 20 phút/tuần**; tỉ lệ ca bị khiếu nại trùng lịch bận giảm về 0%. |
| Phương án không dùng AI | Google Form chuẩn hóa đầu vào + Google Sheets sử dụng công thức Constraint Solver (Rule-based) để tự động ghép ca theo bộ quy tắc logic cố định. |
| Giả thuyết về AI (nếu có) | Dùng AI để trích xuất nguyện vọng từ tin nhắn text tự do trên Zalo/Messenger thành dữ liệu cấu trúc cho phần Rule xử lý ghép ca. |
| Cảm nhận nhanh | Workflow |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — 150 phút/tuần

[1. Thu thập lịch rảnh qua Form/Zalo: 30'] → [2. Nhập liệu vào Excel: 20']
→ [3. Thử sai & Ghép lịch thủ công: 60'] ← BOTTLENECK
→ [4. Kiểm tra xung đột & sót ca: 25'] → [5. Công bố & Điều chỉnh: 15']
---

```text

```

### Problem Card #2

| Trường | Nội dung |
|---|---|
| Job Story | Khi nhân viên gửi lịch rảnh rải rác qua tin nhắn văn bản trên Zalo, tôi muốn tự động trích xuất lịch đăng ký vào bảng tổng hợp, để không phải đọc và chép tay từng dòng. |
| Actor | Quản lý cửa hàng / Trưởng nhóm phụ trách ca trực |
| Thời điểm / bối cảnh | Thứ Sáu – thứ Bảy khi nhân viên gửi lịch rảnh đăng ký ca |
| Quy trình hiện tại (3–7 bước) | 1. Mở từng tin nhắn Zalo của 8–10 nhân viên (15') → 2. Đọc và dịch mong muốn/lịch học của từng người (15') → 3. Nhập tay từng ô vào bảng Excel (20') |
| Bottleneck (bước nào, mất bao nhiêu phút) | **Bước 3: Nhập tay vào Excel** (mất 20 phút và dễ nhập sai thông tin). |
| Impact (nếu không giải thì sao) | Tốn 50 phút/tuần; hay bị sót tin nhắn hoặc ghi sai ca rảnh của nhân viên. |
| Success metric (baseline → target) | Baseline: **50 phút/tuần** → Target: **dưới 5 phút/tuần** (chỉ cần nhấn duyệt kiểm tra). |
| Phương án không dùng AI | Ép nhân viên 100% phải điền đúng mẫu Google Form, không nhận tin nhắn rải rác. |
| Giả thuyết về AI (nếu có) | Dùng AI LLM parsing dữ liệu tin nhắn tự do (vd: "Thứ 2 rảnh sáng, thứ 4 bận cả ngày") ra file JSON/Excel. |
| Cảm nhận nhanh | Workflow |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — 50 phút/tuần
 
[1. Mở từng tin nhắn Zalo của 8–10 NV: 15'] → [2. Đọc và dịch mong muốn/lịch học: 15']
→ [3. Nhập tay từng ô vào Excel: 20'] ← BOTTLENECK

```

# [Problem Card #3] 

| Trường | Nội dung |
|---|---|
| **Job Story** | Khi có nhân viên báo nghỉ đột xuất trước ca làm 2 tiếng, tôi muốn tự động tìm và gợi ý danh sách nhân viên rảnh đang đủ điều kiện, để không phải nhắn tin hỏi từng người trong nhóm. |
| **Actor** | Quản lý ca trực, Nhân viên part-time |
| **Thời điểm / bối cảnh** | Khi phát sinh sự cố xin nghỉ đột xuất trong tuần |
| **Quy trình hiện tại (3–7 bước)** | 1. Nhận thông tin nghỉ (2') $\rightarrow$ 2. Mở file lịch tuần để lọc xem ai rảnh ca đó (10') $\rightarrow$ 3. Nhắn tin/gọi điện hỏi 3-4 ứng viên (20') $\rightarrow$ 4. Cập nhật lại lịch trực (5') |
| **Bottleneck (bước nào, mất bao nhiêu phút)** | Bước 3: Nhắn tin/gọi điện hỏi từng người (mất 20 phút chờ phản hồi). |
| **Impact (nếu không giải thì sao)** | Thiếu nhân sự trong ca làm, ảnh hưởng đến vận hành cửa hàng; quản lý mất thời gian điều phối gấp. |
| **Success metric (baseline $\rightarrow$ target)** | Baseline: 37 phút/lần $\rightarrow$ Target: dưới 5 phút/lần. |
| **Phương án không dùng AI** | Tạo bảng danh sách nhân viên rảnh cố định và quy định thứ tự gọi thay ca bằng Rule tự động gửi thông báo hàng loạt. |
| **Giả thuyết về AI (nếu có)** | AI phân tích mức độ ưu tiên (số giờ đã làm trong tuần, khoảng cách di chuyển) để đề xuất 2 người tối ưu nhất. |
| **Cảm nhận nhanh** | Rule |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — 37 phút/lần
 
[1. Nhận thông tin nghỉ: 2'] → [2. Lọc file lịch tuần xem ai rảnh: 10']
→ [3. Nhắn tin/gọi điện hỏi 3–4 ứng viên: 20'] ← BOTTLENECK
→ [4. Cập nhật lại lịch trực: 5']
```

### Card muốn pitch nhất

- Card số: Card #1 (Tối ưu lịch làm part-time hằng tuần).
- Vì sao: Đây là vấn đề có tác động lớn nhất (tốn 150 phút/tuần), quy trình lặp lại đều đặn, có chỉ số baseline rõ ràng và thể hiện rõ sự kết hợp giữa Rule logic và Workflow.
- Câu hỏi muốn nhóm phản biện:
  1. Bài toán ghép ca này chỉ cần dùng Google Sheets Constraint Solver (Rule) là đủ hay thật sự cần đến sự can thiệp của AI?
  2. Thước đo giảm từ 150 phút xuống dưới 20 phút có khả thi không khi quản lý vẫn phải dành thời gian review lại lịch?

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|---|---|---|
| Baseline 150 phút chỉ là ước lượng tính nhẩm, chưa bấm giờ thực tế. | Đồng ý | Đã ghi chú cách đo: tính tổng thời gian từ lúc mở file gom Form đến lúc xuất bảng thông báo qua 2 tuần làm việc gần nhất. |
| Bài toán ghép ca là toán tối ưu ràng buộc (Constraint Optimization), dùng AI sinh văn bản (LLM) dễ bị sai số ca/lịch bận. | Đồng ý | Chuyển mức độ can thiệp chính sang Rule/Workflow, AI chỉ hỗ trợ xử lý ngôn ngữ ở khâu đọc tin nhắn đầu vào (nếu có). |
| Chưa có boundary rõ ràng, nếu AI/Hệ thống tự gửi lịch mà xếp sai thì ai chịu trách nhiệm? | Đồng ý | Thêm ranh giới (Boundary): Hệ thống chỉ xuất bản nháp gợi ý; Quản lý bắt buộc phải review và duyệt tay trước khi phát hành lịch. |

---

## 4. Tôi đã tham gia phần nào (CP3 → CP7)

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch Problem Card | Đề xuất 2 candidate trong buổi pitch nhóm: #4 (kiểm tra checklist dài, biết mục đã/chưa kiểm tra) và #5 (nắm yêu cầu, thay đổi của tính năng mới để xác định phạm vi test). | Hai candidate được đưa vào bảng pitch và xếp vào cluster A, C của nhóm; không vào shortlist cuối. |
| Phản biện bài của bạn khác | Câu hỏi tôi đã đặt: (1) Có chắc chắn bug cũ sẽ lặp lại ở phiên bản mới không? (2) Việc tái hiện phụ thuộc vào môi trường hay data? (3) Có cần thiết lập rule tự động mapping giữa bug và commit code không? | [Nhóm đã trả lời / điều chỉnh gì sau các câu hỏi này] |
| Nhận phản biện | Câu hỏi tôi nhận được: "Dùng công cụ checklist thông thường có giải quyết được không?" (#4) và "Thông tin phân tán ở nhiều nơi, AI đọc có bị sót ngữ cảnh không?" (#5), cả hai từ Minh. |  |
| Gom cluster / cây OST | Trực tiếp nhóm các bài toán kiểm thử thành 3 Cluster (Tra cứu thông tin, Tái hiện lỗi, Đồng bộ giao tiếp); đóng góp ý kiến loại bỏ các solution đội lốt trong OST |  |
| Chọn candidate problem |  |  |
| Kiểm chứng / research | Phỏng vấn QA (Senior QA Tester), tra cứu 5 ticket Jira bug ngẫu nhiên, research các công cụ Jam, Sentry/Rollbar, Crashlytics/Instabug và pattern Reproduction Test Builder. | Cho thấy tín hiệu ban đầu: 2/2 người xác nhận mất khoảng 30–45 phút/bug, 4/5 ticket thiếu bước tái hiện; nhóm thu hẹp bài toán về "gợi ý 2–3 kịch bản tái hiện". |
| Quy trình nhóm | Tham gia vẽ quy trình hiện tại (5 bước, baseline 40 phút/bug) và quy trình tương lai (~20 phút/bug). | Xác định bottleneck là bước thử sai điều kiện kiểm thử. [Dung bổ sung phần cụ thể mình vẽ] |


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
