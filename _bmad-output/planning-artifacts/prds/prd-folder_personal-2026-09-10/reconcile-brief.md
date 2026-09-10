---
title: "Đối chiếu PRD với Brief + Addendum"
created: 2026-09-10
---

# Đối chiếu: PRD (`prd.md`) vs. Brief (`brief.md`) + Addendum (`addendum.md`)

Nguồn đầu vào:
1. `../../briefs/brief-folder_personal-2026-09-10/brief.md`
2. `../../briefs/brief-folder_personal-2026-09-10/addendum.md`
3. `prd.md` (tài liệu phái sinh)

Kết luận chung: phần lớn số liệu, quyết định và tông giọng của brief/addendum đã được PRD kế thừa trung thực (tiêu chí thành công, cơ chế kiếm tiền theo giai đoạn, disclaimer/disclosure, non-goals, các giả định follow-rate/Google Flow/hoa hồng...). Tìm thấy **3 khoảng trống đáng kể** dưới đây — không phải mâu thuẫn cố ý mà có vẻ bị rơi rụng khi PRD mở rộng sang FR/UJ.

## Gap 1 — Ngưỡng follower để *đủ điều kiện đăng ký* affiliate (Shopee/TikTok Shop) không được đưa vào PRD như điều kiện gating

**Nguồn:** `addendum.md` §"Shopee Affiliate (VN)" — điều kiện ≥500 follower + KYC (CCCD + tài khoản ngân hàng chính chủ); §"TikTok Shop Affiliate (VN)" — ngưỡng chuẩn 1.000 follower để làm Affiliate chính thức (dưới ngưỡng dùng tạm "chia sẻ link ngoài").

**Vấn đề:** PRD (FR-8, FR-9, FR-10, và Phase 2/3 ở §6.1) mô tả việc gắn affiliate link theo giai đoạn nội dung, nhưng không hề đề cập điều kiện tiên quyết để *được phép* tham gia các chương trình affiliate này (số follower tối thiểu, KYC). FR-5 chỉ gate việc mở Nhóm theo follower Threads, không gate việc đăng ký Shopee/TikTok Shop Affiliate. Đây là một ràng buộc vận hành cụ thể, có số liệu rõ ràng trong addendum, nhưng không xuất hiện ở đâu trong PRD như một điều kiện/rủi ro cần theo dõi trước khi Phase 2 (affiliate PCOS/TTC) có thể thực sự vận hành.

## Gap 2 — Kế hoạch hiệu chỉnh lại mốc doanh thu sau 4-6 tuần vận hành thực tế bị bỏ qua

**Nguồn:** `addendum.md` §"Cách tính mốc 'đơn hàng affiliate'": "Đây là ước tính để có mục tiêu tham chiếu ban đầu, **cần hiệu chỉnh lại sau 4-6 tuần vận hành thực tế** khi có dữ liệu hoa hồng/đơn hàng thật."

**Vấn đề:** PRD kế thừa đúng con số giả định (~20.000-25.000đ/đơn) ở SM-3 và ở Danh mục giả định (§9), nhưng bỏ mất phần quan trọng đi kèm: cam kết sẽ **hiệu chỉnh lại** mốc SM-3 sau 4-6 tuần có dữ liệu thật. §8 "Câu hỏi mở" của PRD tuyên bố "không còn câu hỏi mở mang tính phase-blocker" và liệt kê 4 câu hỏi đã chốt (nhịp TikTok, follower thật/bot, giám sát Nhóm, ngưỡng mở Nhóm) — không có câu nào về việc recalibrate SM-3. Nếu không ghi nhận việc này ở đâu đó (Open Questions hoặc một cột mốc theo dõi), mốc doanh thu ước tính có nguy cơ bị đóng băng như một con số cứng thay vì được xem là ước tính tạm cần cập nhật như addendum chủ định.

## Gap 3 — Công cụ AI cho viết kịch bản (Claude Team, Gemini) trong phần Giải pháp của brief không xuất hiện trong PRD

**Nguồn:** `brief.md` §"Giải pháp": "Người thực hiện tận dụng các công cụ AI sẵn có (**Claude Team, Gemini để viết kịch bản**; Google Flow bản miễn phí để tạo video/giọng đọc) để một mình vận hành đa kênh..."

**Vấn đề:** PRD chi tiết hóa phần công cụ sản xuất video (FR-11: Google Flow, kèm assumption về free tier) nhưng không đề cập gì đến công cụ viết kịch bản/nội dung (Claude Team, Gemini) dù đây là một phần ngang hàng của cùng câu giải pháp trong brief và là yếu tố then chốt cho việc một người vận hành đa kênh nổi. Vì PRD đã chọn "nâng cấp" phần Google Flow thành một FR + assumption riêng, việc bỏ hoàn toàn phần kịch bản/viết nội dung bằng AI tạo cảm giác rơi rụng không chủ đích hơn là một quyết định thu hẹp phạm vi có chủ ý (không có ghi chú non-goal nào giải thích lý do loại trừ).

## Ghi chú thêm (không tính là gap, chỉ để tham khảo)

- Số liệu phân bổ độ tuổi audience thật (25-34 tuổi: 69,5%; 18-24 tuổi: 20,6%) từ Threads Insights trong brief §"Đối tượng phục vụ" không được nhắc lại trong PRD §2 (PRD chỉ mô tả JTBD + 3 persona minh họa không gắn tuổi cụ thể). Vì PRD đã đánh dấu rõ tên nhân vật là minh họa và giữ đúng tinh thần hành vi, đây được xem là rút gọn hợp lý chứ không phải mất mát nội dung — nêu ở đây chỉ để người review cân nhắc nếu muốn giữ số liệu định lượng gốc làm căn cứ.
