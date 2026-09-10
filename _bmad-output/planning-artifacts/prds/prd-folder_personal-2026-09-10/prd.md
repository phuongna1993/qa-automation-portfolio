---
title: "Hành Trình Mẹ & Bé — PRD"
status: final
created: 2026-09-10
updated: 2026-09-10
---

# PRD: Hành Trình Mẹ & Bé

## 0. Mục đích tài liệu

Tài liệu này chi tiết hóa [brief.md](../../briefs/brief-folder_personal-2026-09-10/brief.md) (đã `final`) thành các yêu cầu nội dung và vận hành cụ thể cho chiến lược tiếp thị liên kết đa kênh "Hành Trình Mẹ & Bé". Không có phần mềm/công cụ nội bộ nào cần xây trong phạm vi này — mọi "tính năng" ở đây là quy tắc nội dung, quy trình vận hành, và cơ chế tăng trưởng/kiếm tiền mà người vận hành (một mình, dùng AI hỗ trợ) thực hiện thủ công trên Threads, Facebook, TikTok. Chi tiết nghiên cứu chính sách nền tảng nằm ở `addendum.md` đi kèm brief; PRD này không lặp lại.

## 1. Vision

Xây dựng một hệ sinh thái nội dung cá nhân, danh tính thật, kể lại hành trình buồng trứng đa nang (PCOS) → thay đổi lối sống → chuẩn bị mang thai → sinh đẻ → nuôi con, để trở thành nguồn thông tin đáng tin cậy cho phụ nữ Việt Nam đang ở từng giai đoạn đó — thay vì lý thuyết y khoa khô khan hay quảng cáo TPCN trá hình. Threads là điểm chạm đầu tiên; nhóm Facebook là nơi cộng đồng "sở hữu" được nuôi dưỡng sâu hơn; TikTok mở rộng sang định dạng video. Doanh thu đến từ tiếp thị liên kết, luôn tách bạch khỏi nội dung y tế nhạy cảm.

## 2. Đối tượng phục vụ

### 2.1 Nhu cầu cốt lõi (Jobs To Be Done)
- Hiểu đúng về PCOS từ một người đã thực sự trải qua, thay vì thông tin nhiễu hoặc quảng cáo trá hình.
- Cảm thấy không đơn độc khi đối mặt với một chủ đề nhạy cảm liên quan đến khả năng sinh sản.
- Tìm được hướng đi cụ thể (chế độ ăn uống/sinh hoạt) để cải thiện khả năng có con tự nhiên.

### 2.2 Ngoài phạm vi (v1)
Nam giới; phụ nữ không liên quan đến PCOS/kế hoạch sinh sản; độc giả tìm tư vấn y khoa thay thế bác sĩ (kênh này không đóng vai trò đó — xem FR-13).

### 2.3 Hành trình người dùng chính

- **UJ-1. Mai khám phá thụ động qua tìm kiếm.** [ASSUMPTION: tên minh họa, hành vi đã được xác nhận] Mai chưa có nhu cầu sinh con ngay, vừa biết mình bị PCOS, chưa có kiến thức gì. Cô lướt Threads, gõ tìm cụm từ "pcos", thấy một bài chia sẻ hiện ra. Đọc xong, có thể để lại bình luận hoặc không. Nếu nội dung đúng với tình trạng của mình, cô vào trang cá nhân đọc thêm các bài khác; nếu các bài được nối thành series, cô bắt đầu theo dõi. Khi đã đủ tin tưởng qua nhiều bài, cô tìm nhóm Facebook liên quan để follow và chia sẻ tiếp.
- **UJ-2. Trang chủ động hỏi, được tiếp cận qua bình luận.** [ASSUMPTION: tên minh họa, hành vi đã được xác nhận] Cùng hoàn cảnh (mới biết PCOS, chưa có kiến thức), nhưng thay vì tìm bài có sẵn, Trang tự đăng một bài trên Threads hỏi ý kiến cộng đồng về PCOS. Người vận hành chủ động tìm thấy bài này và để lại bình luận có giá trị (tăng tương tác cho cả hai phía). Trang ghé xem trang cá nhân của người vận hành từ bình luận đó, và follow.
- **UJ-3. Hương đã có kiến thức, đang cố có con.** [ASSUMPTION: tên minh họa, hành vi đã được xác nhận] Đã bị PCOS, có nhu cầu sinh sản, đã có kiến thức cơ bản (khác UJ-1/UJ-2 vốn "chưa có kiến thức gì"). Hương tiếp tục chủ động tìm và đọc các bài PCOS chuyên sâu hơn để tìm hiểu thêm hướng có con. Cùng đích đến như UJ-1: follow / vào nhóm Facebook.
- **UJ-4. Mai (đã vào Nhóm) mua sản phẩm qua affiliate link.** [ASSUMPTION: nối tiếp UJ-1, hành vi mua hàng chưa được xác nhận bằng dữ liệu thực tế] Vài tuần sau khi vào Nhóm ở cuối UJ-1, Mai đọc một bài ghim/bài mới trong Nhóm giới thiệu một cuốn sách "chuẩn bị mang thai" kèm nhận xét cá nhân của người vận hành và disclosure affiliate rõ ràng (FR-13). Vì đã tin tưởng qua nhiều tuần theo dõi, Mai bấm link rút gọn trong bài (FR-10), được điều hướng sang Shopee, và đặt mua. Đây là hành trình duy nhất chạm tới doanh thu (SM-3) — không có nó, các UJ khác chỉ dừng ở "follow/vào nhóm" mà không giải thích tiền đến từ đâu.

Bốn hành trình hội tụ hoặc nối tiếp nhau: UJ-1/UJ-2/UJ-3 đưa người đọc đến điểm follow/vào nhóm, khác nhau ở **kênh tiếp cận** (search thụ động vs. bình luận chủ động) và **độ sâu nội dung cần** (nhập môn vs. chuyên sâu); UJ-4 tiếp nối từ đó đến hành vi mua hàng — đây là căn cứ trực tiếp cho Features ở mục 4, đặc biệt là 4.3.

## 3. Thuật ngữ

- **PCOS** — Hội chứng buồng trứng đa nang (Polycystic Ovary Syndrome), chủ đề nội dung cốt lõi của giai đoạn đầu hành trình.
- **Giai đoạn PCOS/TTC** — Giai đoạn đầu hành trình: từ lúc phát hiện PCOS đến khi đang cố gắng có con (Trying To Conceive), tương ứng tháng 1-3 của lộ trình.
- **Giai đoạn Mang thai/Sau sinh** — Giai đoạn sau của hành trình: mang thai, sinh đẻ, nuôi con, tương ứng tháng 4 trở đi.
- **Series** — Chuỗi bài đăng có liên kết nội dung với nhau, mỗi bài gợi ý phần tiếp theo, tạo lý do để follow.
- **Nhóm** — Nhóm Facebook riêng, nơi cộng đồng được nuôi dưỡng sâu hơn Threads và là nơi chính đặt affiliate link.
- **Follower thật** — Người theo dõi thật, phân biệt với follower ảo/mua; đo qua Threads Insights.
- **Disclosure** — Công bố rõ ràng quan hệ tiếp thị liên kết trên nội dung có gắn link, theo quy định FTC/Meta (chi tiết ở `addendum.md`).
- **Disclaimer y tế** — Câu công bố "đây là trải nghiệm cá nhân, không thay thế tư vấn bác sĩ" bắt buộc trên nội dung chia sẻ trải nghiệm.

## 4. Features

### 4.1 Growth Engine trên Threads

**Mô tả:** Cơ chế nội dung và tương tác trên Threads để chuyển người đọc ngẫu nhiên thành follower thật, phục vụ cả ba hành trình UJ-1, UJ-2, UJ-3. Kịch bản/nội dung bài viết được soạn với sự hỗ trợ của Claude Team và Gemini (viết, biên tập, lên ý tưởng series).

**Yêu cầu:**

#### FR-1: Nội dung dạng series có liên kết
Người vận hành đăng bài theo cấu trúc series, mỗi bài kết thúc bằng gợi ý rõ ràng cho phần tiếp theo. Realizes UJ-1, UJ-3.

**Kết quả kiểm chứng được:**
- Mỗi bài thuộc một series có ghi chú thứ tự (VD: "Phần 2/5") hoặc gợi ý bài tiếp theo.
- Duy trì tần suất 1 bài/ngày, không đứt quãng quá 2 ngày liên tiếp (theo brief).

#### FR-2: Chủ động tìm và bình luận trên bài PCOS của người khác
Người vận hành định kỳ tìm kiếm từ khóa liên quan PCOS trên Threads, xác định các bài người dùng khác đang hỏi/chia sẻ, và để lại bình luận có giá trị thật (không spam link). Realizes UJ-2.

**Kết quả kiểm chứng được:**
- Bình luận không chứa link affiliate hoặc lời mời follow trực tiếp (giữ đúng vai trò UJ-2: tăng tương tác, để người đọc tự tìm đến trang cá nhân).

**Phạm vi không bao gồm:** Không nhắn tin riêng (DM) chào mời — ngoài phạm vi v1.

#### FR-3: Nội dung phân tầng theo mức hiểu biết
Nội dung được chia rõ giữa tầng nhập môn (dành cho UJ-1/UJ-2: mới biết, chưa có kiến thức) và tầng chuyên sâu (dành cho UJ-3: đã có kiến thức cơ bản, đang tìm cách có con). Realizes UJ-1, UJ-3.

**Kết quả kiểm chứng được:**
- Mọi bài thuộc tầng nhập môn gắn hashtag `#PCOS101`; mọi bài thuộc tầng chuyên sâu gắn hashtag `#PCOSTTC` — quy tắc cố định, không suy đoán khi audit.

#### FR-4: Bio và CTA tối ưu chuyển đổi
Bio Threads nêu rõ giá trị nội dung và lời mời follow; khi nhóm Facebook đã mở (FR-5), bio bổ sung link tới nhóm. Realizes UJ-1, UJ-2, UJ-3.

**Kết quả kiểm chứng được:**
- Bio luôn cập nhật link hiện hành (nhóm Facebook khi đã mở).

### 4.2 Cộng đồng (Nhóm Facebook)

**Mô tả:** Nơi "sở hữu" cộng đồng sâu hơn Threads, mở đúng thời điểm theo lộ trình 3 pha trong brief.

**Yêu cầu:**

#### FR-5: Ngưỡng mở Nhóm
Nhóm chỉ được mở khi Threads đã đạt ngưỡng follower đủ để seed (theo Phase 2 trong brief, ước lượng gần mốc 3 tháng ≥1.000-1.500 follower).

**Kết quả kiểm chứng được:**
- Nhóm không được công bố công khai trước khi Threads đạt tối thiểu 1.000 follower thật (ngưỡng dưới của khoảng ≥1.000-1.500 đã chốt).

#### FR-6: Nội quy và nội dung ghim
Nhóm có bài ghim chứa nội quy, disclaimer y tế (FR-12), và disclosure affiliate (FR-13).

**Kết quả kiểm chứng được:**
- Bài ghim nội quy tồn tại và hiển thị ở đầu Nhóm ngay từ ngày mở (cùng thời điểm với FR-5).

#### FR-7: Cầu nối Threads → Nhóm
Lời mời vào nhóm luôn kèm lý do cụ thể ("vì sao nên vào nhóm"), không chỉ dán link trần.

**Kết quả kiểm chứng được:**
- Mọi bài Threads mời vào Nhóm chứa ít nhất một câu nêu lý do cụ thể, không chỉ có link trần.

#### FR-15: Duyệt bài trước khi đăng trong Nhóm
Nhóm bật chế độ duyệt bài viết của thành viên trước khi hiển thị công khai, để bù cho việc người vận hành một mình không thể giám sát liên tục.

**Kết quả kiểm chứng được:**
- Cài đặt nhóm ở chế độ "yêu cầu quản trị viên duyệt bài viết" được bật ngay khi mở nhóm (FR-5).

### 4.3 Cơ chế kiếm tiền theo giai đoạn

**Mô tả:** Affiliate link luôn gắn theo đúng giai đoạn hành trình của người đọc, tách biệt khỏi nội dung PCOS trực tiếp (xem FR-14), phục vụ hành trình UJ-4.

**Yêu cầu:**

#### FR-16: Ngưỡng kích hoạt affiliate
Trước khi đăng ký hoặc kích hoạt bất kỳ chương trình affiliate nào, tài khoản phải đạt ngưỡng follower tối thiểu của chương trình tương ứng (chi tiết chính sách ở `addendum.md`).

**Kết quả kiểm chứng được:**
- Đăng ký Shopee Affiliate chỉ thực hiện khi Threads đạt ≥500 follower thật.
- Đăng ký TikTok Shop Affiliate (trạng thái chính thức) chỉ thực hiện khi kênh TikTok đạt ≥1.000 follower; dưới ngưỡng này, dùng tính năng "chia sẻ link ngoài" thay thế, không chặn FR-8/FR-9.

#### FR-8: Affiliate giai đoạn PCOS/TTC
Trong nội dung/giai đoạn PCOS/TTC, chỉ gắn affiliate sản phẩm hỗ trợ lối sống không ngụ ý điều trị: sách "chuẩn bị mang thai", dụng cụ theo dõi rụng trứng, thực phẩm sạch, đồ tập yoga. Realizes UJ-4.

**Kết quả kiểm chứng được:**
- Mọi sản phẩm gắn link trong giai đoạn này thuộc một trong 4 nhóm đã liệt kê; không có sản phẩm nào ngụ ý điều trị/chữa PCOS (đối chiếu FR-14).

#### FR-9: Affiliate giai đoạn Mang thai/Sau sinh
Trong nội dung/giai đoạn Mang thai/Sau sinh, gắn affiliate đồ dùng mẹ & bé: đồ ăn dặm, sách cho bé, đồ chơi.

**Kết quả kiểm chứng được:**
- Không có link affiliate đồ mẹ & bé nào xuất hiện trong nội dung được gắn hashtag `#PCOS101`/`#PCOSTTC` (FR-3) — giữ đúng ranh giới giai đoạn.

#### FR-10: Quản lý link Shopee qua bio-link
Vì Shopee chưa tích hợp trực tiếp Threads/TikTok, mọi link Shopee đi qua công cụ rút gọn/bio-link (Flyn/beacons.ai/bio.link), đặt ở bio hoặc ghim trong Nhóm — không dán link Shopee trần trong bài Threads. Realizes UJ-4.

**Kết quả kiểm chứng được:**
- Không có URL Shopee dạng đầy đủ (shopee.vn/...) xuất hiện trực tiếp trong nội dung bài Threads; chỉ xuất hiện dưới dạng link rút gọn ở bio/bài ghim Nhóm.

### 4.4 Mở rộng TikTok

**Mô tả:** Kênh TikTok duy nhất, kết hợp kể chuyện cho bé bằng AI và review sách cho bé, ra mắt sau khi Nhóm đã có nhịp (Phase 3 trong brief).

**Yêu cầu:**

#### FR-11: Sản xuất nội dung TikTok bằng AI
Kịch bản truyện/nội dung review được soạn bằng Claude Team và Gemini; video/giọng đọc được sản xuất bằng Google Flow bản miễn phí trước [ASSUMPTION: Google Flow free tier đủ để sản xuất video đều đặn — chưa kiểm chứng thực tế], chỉ cân nhắc công cụ trả phí nếu free tier không đáp ứng được chất lượng/số lượng cần thiết.

**Kết quả kiểm chứng được:**
- Kênh ra mắt với tối thiểu 10-15 video đã chuẩn bị trước khi công bố công khai (theo brief).
- Sau khi ra mắt, duy trì tần suất 7 video/tuần (~1 video/ngày), cùng nhịp với Threads.

**Feature-specific NFRs:**
- Nội dung không được là bản sao/template trùng lặp của nội dung trên kênh Threads/Nhóm — tránh rủi ro chính sách nội dung AI hàng loạt của TikTok (xem `addendum.md`).

### 4.5 Tuân thủ & niềm tin

**Mô tả:** Áp dụng xuyên suốt mọi kênh, không thuộc riêng feature nào — ranh giới giữ cho toàn bộ chiến lược an toàn về mặt pháp lý/uy tín.

**Yêu cầu:**

#### FR-12: Disclaimer y tế bắt buộc
Mọi nội dung chia sẻ trải nghiệm cá nhân (Threads, Nhóm, TikTok) đi kèm disclaimer: "đây là trải nghiệm cá nhân, không thay thế tư vấn bác sĩ."

**Kết quả kiểm chứng được:**
- 100% bài/video chia sẻ trải nghiệm cá nhân có câu disclaimer nguyên văn hoặc tương đương rõ nghĩa (SM-C1).

#### FR-13: Disclosure affiliate bắt buộc
Mọi bài/video có gắn affiliate link công bố rõ quan hệ tiếp thị liên kết, theo quy định FTC/Meta.

**Kết quả kiểm chứng được:**
- 100% bài/video có link affiliate (Shopee/TikTok Shop) chứa nhãn công bố quan hệ hợp tác (VD: "#quảng cáo", "link tiếp thị liên kết") (SM-C1).

#### FR-14: Tách bạch nội dung y tế và affiliate
Không bao giờ gắn affiliate link vào bài/video nói trực tiếp về hiệu quả điều trị/cải thiện PCOS — affiliate chỉ xuất hiện ở nội dung sản phẩm hỗ trợ lối sống hoặc mẹ & bé (FR-8, FR-9), không ở nội dung khẳng định hiệu quả y tế.

**Kết quả kiểm chứng được:**
- 0 bài/video vừa khẳng định "tôi đã cải thiện/khỏi triệu chứng PCOS nhờ [sản phẩm]" vừa gắn affiliate link của chính sản phẩm đó — trải nghiệm cá nhân (không link) và giới thiệu sản phẩm hỗ trợ lối sống (có link, không khẳng định hiệu quả điều trị) luôn là hai bài tách biệt (SM-C2).

## 5. Non-Goals (Rõ ràng loại trừ)

- Không xây dựng phần mềm/công cụ nội bộ nào (bảng theo dõi, dashboard, script tự động hóa) trong phạm vi PRD này.
- Không mở kênh YouTube truyện kể trong giai đoạn này — RPM thấp và rủi ro chính sách nội dung AI cho trẻ em cao (xem brief §Rủi ro).
- Không mở thêm kênh TikTok chủ đề khác (đồ ăn dặm, v.v.) trong giai đoạn này.
- Không thuê ngoài/cộng tác viên trong 6 tháng đầu — vận hành một mình.
- Không dùng danh tính ẩn danh trên bất kỳ kênh nào.
- Không định vị kênh như một nguồn tư vấn y khoa thay thế bác sĩ.

## 6. Phạm vi (v1)

### 6.1 Trong phạm vi
- Phase 1: Ổn định Threads (FR-1 đến FR-4).
- Phase 2: Mở Nhóm Facebook (FR-5 đến FR-7, FR-15) + bắt đầu affiliate giai đoạn PCOS/TTC (FR-16, FR-8, FR-10).
- Phase 3: Ra mắt kênh TikTok (FR-11) + affiliate giai đoạn Mang thai/Sau sinh khi nội dung tới giai đoạn đó (FR-9).
- Tuân thủ (FR-12 đến FR-14) áp dụng xuyên suốt cả 3 phase, từ ngày đầu.

### 6.2 Ngoài phạm vi v1
- Kênh YouTube truyện kể — lùi sang Vision (brief), chờ đánh giá lại rủi ro chính sách.
- Các kênh TikTok chủ đề khác (ăn dặm...) — lùi sau mốc 6 tháng, tùy vào kết quả kênh TikTok đầu tiên.
- [NOTE FOR PM] Thuê ngoài/cộng tác viên — cân nhắc lại nếu doanh thu đạt mốc 6 tháng (5-10 triệu/tháng) theo brief.

## 7. Tiêu chí thành công

**Chính**
- **SM-1**: Threads ≥1.000-1.500 follower thật ở mốc 3 tháng, ≥5.000 ở mốc 6 tháng — đo bằng Threads Insights, chấp nhận không phân biệt được follower ảo/bot ở giai đoạn này [ASSUMPTION]. Kiểm chứng FR-1, FR-2, FR-3, FR-4.
- **SM-2**: Nhóm Facebook ≥300-500 thành viên (3 tháng), ≥1.500-2.000 thành viên có tương tác thật (6 tháng). Kiểm chứng FR-5, FR-6, FR-7.
- **SM-3**: Doanh thu affiliate 1-3 triệu đồng/tháng (~50-100 đơn) ở mốc 3 tháng; 5-10 triệu đồng/tháng (~200-400 đơn) ở mốc 6 tháng [ASSUMPTION: hoa hồng trung bình ~20.000-25.000đ/đơn — xem `addendum.md`]. Kiểm chứng FR-16, FR-8, FR-9, FR-10 (realizes UJ-4). [NOTE FOR PM] Mốc này cần hiệu chỉnh lại sau 4-6 tuần vận hành thực tế khi có dữ liệu hoa hồng/đơn hàng thật (đã nêu trong `addendum.md`), không giữ cứng nếu số liệu thực tế lệch xa giả định.

**Phụ**
- **SM-4**: Kênh TikTok ra mắt với ≥10-15 video (3 tháng); có ít nhất 1 video vượt 10.000 view (6 tháng). Kiểm chứng FR-11.

**Counter-metrics (không tối ưu bằng mọi giá)**
- **SM-C1**: Tỉ lệ bài/video vi phạm ranh giới disclaimer/disclosure (FR-12, FR-13, FR-14) phải bằng 0 — không đánh đổi tốc độ tăng follower hoặc đơn hàng lấy việc bỏ qua disclaimer/disclosure. Đối trọng với SM-1 và SM-3.
- **SM-C2**: Không gắn affiliate link vào nội dung khẳng định hiệu quả điều trị PCOS dù nội dung đó có thể tăng đơn hàng ngắn hạn. Đối trọng với SM-3.

## 8. Câu hỏi mở

Không còn câu hỏi mở mang tính phase-blocker tại thời điểm hoàn thiện PRD. Bốn câu hỏi ban đầu (nhịp độ TikTok, follower thật vs bot, giám sát Nhóm khi offline, ngưỡng mở Nhóm) đã được chốt trong quá trình triage — xem `.memlog.md` để biết lịch sử quyết định.

## 9. Danh mục giả định

- §2.3 UJ-1, UJ-2, UJ-3 — tên nhân vật (Mai, Trang, Hương) là minh họa, chỉ dùng để gắn ngữ cảnh cho hành vi đã được xác nhận; bản thân hành vi/hành trình không phải giả định.
- §4.4 FR-11 — Google Flow bản miễn phí đủ để sản xuất video TikTok đều đặn 7 video/tuần, chưa kiểm chứng thực tế.
- §7 SM-1 — Threads Insights được chấp nhận làm nguồn đo follower thật duy nhất trong giai đoạn này, dù không phân biệt được follower ảo/bot.
- §7 SM-3 — hoa hồng trung bình pha trộn ~20.000-25.000đ/đơn hàng affiliate.
- Kế thừa từ brief: audience giai đoạn PCOS/TTC sẵn sàng mua sản phẩm hỗ trợ lối sống (chưa có dữ liệu chuyển đổi thực tế); tăng tần suất và CTA sẽ cải thiện được tỉ lệ follow hiện tại (~0,6%).
