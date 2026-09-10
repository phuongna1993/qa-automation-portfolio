---
title: 'Reconcile PRD → ARCHITECTURE-SPINE'
type: architecture-review
created: 2026-09-10
sources:
  - '_bmad-output/planning-artifacts/prds/prd-folder_personal-2026-09-10/prd.md'
  - '_bmad-output/planning-artifacts/architecture/architecture-folder_personal-2026-09-10/ARCHITECTURE-SPINE.md'
---

# Reconcile: PRD (16 FR) → ARCHITECTURE-SPINE

## Coverage check — mọi FR có nguy cơ cross-channel/consistency

Tất cả FR-1..FR-16 đều xuất hiện trong `Capability → Architecture Map` của spine, và mọi FR có tính chất "quy tắc dùng chung xuyên kênh" (hashtag, gate, disclaimer/disclosure, tách bạch trần thuật/thương mại, chống trùng nội dung) đều có ít nhất một AD tương ứng (AD-1..AD-6). FR-15 (duyệt bài Nhóm) được spine cố ý không gán AD, kèm lý do rõ ràng (rủi ro thấp, vận hành một mình) — đây là quyết định minh bạch, không phải bỏ sót. Về mặt "có FR nào hoàn toàn không được nhắc tới" — không có; coverage ở mức khung là đầy đủ.

Tuy nhiên, đối chiếu từng dòng phát hiện 3 chỗ spine làm rơi mất chi tiết có tính load-bearing của PRD (số liệu/quy tắc vận hành cụ thể, không phải diễn giải thêm), và 1 chỗ ánh xạ "Governed by" không thực sự khớp với nội dung FR.

## Gaps

### G1 — [Contradiction/Drop nghiêm trọng] Mất điều khoản fallback của FR-16 khi TikTok Shop Affiliate chưa đủ ngưỡng

- **PRD FR-16** (Kết quả kiểm chứng được, dòng 2): "Đăng ký TikTok Shop Affiliate (trạng thái chính thức) chỉ thực hiện khi kênh TikTok đạt ≥1.000 follower; **dưới ngưỡng này, dùng tính năng "chia sẻ link ngoài" thay thế, không chặn FR-8/FR-9**."
- **Spine AD-4, rule 3** (dòng 54): chỉ giữ lại vế ngưỡng ("TikTok Shop Affiliate ... khi kênh TikTok ... ≥1.000 follower — không tính follower Threads"), **không nhắc gì đến cơ chế "chia sẻ link ngoài" thay thế khi dưới ngưỡng, và không nhắc rằng gate này KHÔNG được chặn FR-8/FR-9**.
- **Vì sao load-bearing:** đây không phải chi tiết phụ — nó xác định liệu affiliate mẹ & bé/PCOS-TTC (FR-8, FR-9) có thể vận hành trên TikTok trước khi kênh đạt 1.000 follower hay không. Đọc riêng AD-4 như hiện tại, một người vận hành có thể hiểu nhầm là "affiliate trên TikTok bị khóa hoàn toàn tới khi đủ 1.000 follower", trái với ý PRD là chỉ *trạng thái chính thức* của chương trình bị khóa, còn cơ chế thay thế vẫn chạy. Đây là một gap thật (contradiction-by-omission), không phải diễn giải hợp lệ.
- **Đề xuất:** bổ sung vào AD-4 rule 3 một câu tương đương: "Dưới ngưỡng 1.000 follower TikTok, dùng tính năng chia sẻ link ngoài (affiliate link dạng khác) thay thế trạng thái chính thức — gate này không chặn FR-8/FR-9."

### G2 — [Drop] Ngưỡng dung sai tần suất đăng Threads (FR-1) không được mang sang bảng Consistency Conventions

- **PRD FR-1** (Kết quả kiểm chứng được, dòng 61): "Duy trì tần suất 1 bài/ngày, **không đứt quãng quá 2 ngày liên tiếp** (theo brief)."
- **Spine, bảng Consistency Conventions** (dòng 87): "Nhịp đăng cố định theo kênh: Threads 1 bài/ngày, TikTok 7 video/tuần sau khi ra mắt." — chỉ còn "1 bài/ngày", mất hẳn dung sai "không đứt quãng quá 2 ngày liên tiếp".
- **Vì sao đáng chú ý:** bảng Consistency Conventions là nơi spine dùng để chuẩn hóa quy tắc audit xuyên kênh; nếu chỉ đọc bảng này (không quay lại PRD), người vận hành hoặc AI hỗ trợ có thể áp dụng sai tiêu chí (coi mọi khoảng trống >1 ngày là vi phạm, thay vì dung sai ≤2 ngày liên tiếp mà PRD cho phép).
- **Đề xuất:** sửa dòng cadence thành "Threads 1 bài/ngày (dung sai: không đứt quãng quá 2 ngày liên tiếp)".

### G3 — [Ánh xạ không khớp] FR-7 (lời mời vào Nhóm phải kèm lý do, không link trần) không thực sự được AD nào bảo vệ

- **PRD FR-7** (dòng 101-105): "Lời mời vào nhóm luôn kèm lý do cụ thể... không chỉ dán link trần." Kết quả kiểm chứng: "Mọi bài Threads mời vào Nhóm chứa ít nhất một câu nêu lý do cụ thể, không chỉ có link trần."
- **Spine, Capability Map** (dòng 109): FR-5..FR-7 → "Governed by: AD-2, AD-4". Nhưng AD-2 chỉ nói về disclaimer/disclosure, AD-4 chỉ nói về stage-gate follower/video — **không AD nào trong hai cái này thực sự mã hóa quy tắc "lời mời phải có lý do, không chỉ link trần"**.
- **So sánh để thấy rõ đây là gap thật, không phải diễn giải hợp lệ:** quy tắc "không link trần" tương tự ở FR-10 (Shopee) *có* được đưa vào bảng Consistency Conventions ("không dán link Shopee trần trong bài Threads"), nhưng quy tắc "không link trần" ở FR-7 (mời vào Nhóm) thì không xuất hiện ở bất kỳ đâu trong spine ngoài việc bị gán nhầm cho AD-2/AD-4. Đây là xử lý không nhất quán giữa hai FR có hình dạng quy tắc giống nhau.
- **Đề xuất:** hoặc (a) thêm FR-7 vào bảng Consistency Conventions cạnh quy tắc FR-10 ("Lời mời vào Nhóm luôn kèm lý do cụ thể, không dán link trần"), hoặc (b) sửa cột Governed by của dòng FR-5..FR-7 để không ngụ ý AD-2/AD-4 bao phủ yêu cầu này.

## Không flag (đã cân nhắc, không phải gap)

- AD-3 thêm hashtag `#MeVaBe` cho giai đoạn Mang thai/Sau sinh dù PRD không đặt tên hashtag đó — đúng như đề bài loại trừ, đây là việc spine operationalize một khoảng trống PRD để lại (FR-9 chỉ nói "giai đoạn Mang thai/Sau sinh" mà không có hashtag cụ thể), không phải mâu thuẫn.
- Disclosure "#quảngcáo" (spine, không dấu cách) so với PRD "#quảng cáo" (có dấu cách) — hashtag hợp lệ không được chứa khoảng trắng, sửa này là chỉnh lỗi hợp lý khi thao tác hóa, không phải làm sai lệch nội dung.
- AD-2 và AD-5 mở rộng phạm vi từ "Threads/Nhóm/TikTok" (PRD liệt kê tường minh cho FR-12/13) sang "mọi kênh kể cả kênh mở sau này" — mở rộng hợp lý, nhất quán với tinh thần FR-14 vốn đã không giới hạn kênh.
- FR-15 không có AD riêng — spine nêu lý do rõ ràng (rủi ro thấp, một mình vận hành), không phải bỏ sót im lặng như G3.
- FR-11's điều kiện "chỉ cân nhắc công cụ trả phí nếu free tier không đáp ứng" bị rút gọn thành ghi chú assumption ở bảng Nền tảng & Công cụ — cân nhắc nhưng đánh giá là chi tiết vận hành nhỏ, không ảnh hưởng đến bất kỳ AD hay stage-gate nào, nên không liệt kê thành gap chính thức.

## Kết luận

Spine bao phủ đúng cấu trúc và đa số chi tiết định lượng (ngưỡng follower 1.000/500/1.000, số video 10-15, 7 video/tuần, nguyên văn disclaimer) một cách chính xác. Ba gap nêu trên (G1-G3) là các chỗ cụ thể, có thể sửa trực tiếp trong ARCHITECTURE-SPINE.md mà không cần đổi paradigm hay AD nào.
