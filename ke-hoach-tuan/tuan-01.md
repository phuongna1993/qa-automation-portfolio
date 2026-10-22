# Tuần 1 (26/10 - 01/11): Khởi động

**Mục tiêu tuần**
- Cài xong JDK, IntelliJ, git. Học xong L01-L03 và commit bài tập lên GitHub.
- Nắm test process và vẽ được nó gắn với dự án đang làm.
- Có danh sách dự án và thành tích 8 năm để chuẩn bị viết CV.
- Học 48 từ TOEIC (Bài 1-4).

**Khung giờ gợi ý:** ngày thường 20:30-22:00 (tiếng Anh 30' trước, môn chính 60' sau). Cuối tuần 9:00-12:00. Có thể đổi giờ, nhưng nên giữ cố định để thành thói quen.

---

## Chuẩn bị trước Thứ 2 (làm trong Chủ nhật 25/10, khoảng 30')
- [ ] Cài **Anki** (máy tính + điện thoại), tạo deck `TOEIC 600`.
- [ ] Mở tài khoản **dailydictation.com** (hoặc trang chép chính tả tương tự).
- [ ] Tạo file `tien-do.md` hoặc 1 sheet để ghi điểm chép chính tả mỗi buổi.
- [ ] Tải sẵn video **L01-L03** của khóa Java.
- [ ] Trong repo này tạo thư mục `java-basics/` để chứa bài tập Java.

---

## Thứ 2 (26/10)

### Tiếng Anh 30'
| Phút | Việc |
|---|---|
| 0-10 | **Anki: TOEIC Bài 1 *Contracts*:** abide by, agreement, assurance, cancellation, determine, engage, establish, obligate, party, provision, resolve, specific. Mỗi thẻ: mặt trước là từ, mặt sau là nghĩa + 1 câu tự đặt về công việc test |
| 10-30 | **Chép chính tả** (cách làm ở [phần cuối file](#cách-làm-chép-chính-tả-20)) |

### Automation 60': L01
| Phút | Việc |
|---|---|
| 0-25 | Xem L01 phần 1: JDK, JAVA_HOME/PATH, compile và run bằng `javac`/`java`, IDE |
| 25-35 | Tự làm: cài JDK, đặt JAVA_HOME, chạy `java -version`. Viết `Hello.java`, compile và chạy bằng terminal (chưa dùng IDE) |
| 35-55 | Xem L01 phần 2: git init, data type, khai báo biến, camelCase/snake_case, re-declare/re-assign |
| 55-60 | Mở IntelliJ, tạo project `java-basics`, `git init`, commit đầu tiên |

**Kết quả:** chạy được Java bằng terminal và IntelliJ, có commit đầu tiên.

---

## Thứ 3 (27/10)

### Tiếng Anh 30'
| Phút | Việc |
|---|---|
| 0-10 | Anki: ôn Bài 1 + học **Bài 2 *Marketing*:** attract, compare, competition, consume, convince, currently, fad, inspiration, market, persuasion, productive, satisfaction |
| 10-30 | **Shadowing** đoạn self-introduction trong [English/tuan-01.md](../English/tuan-01.md) (cách làm ở cuối file) |

### Kiến thức test 60': Test process
| Phút | Việc |
|---|---|
| 0-30 | Đọc lại **7 hoạt động của test process** (ISTQB Foundation v4.0, mục 1.4): test planning, monitoring & control, analysis, design, implementation, execution, completion |
| 30-60 | Điền bảng dưới đây **theo đúng dự án bạn đang làm** (không chép định nghĩa) |

| Hoạt động | Câu hỏi chính | Input | Output (testware) | Ai làm ở dự án của bạn |
|---|---|---|---|---|
| Planning | Test cái gì, bằng cách nào, khi nào xong? | | | |
| Monitoring & control | Đang đúng tiến độ chưa, cần điều chỉnh gì? | | | |
| Analysis | Test **cái gì** (test condition)? | | | |
| Design | Test **như thế nào** (test case, data)? | | | |
| Implementation | Đã **sẵn sàng** chạy chưa (môi trường, suite)? | | | |
| Execution | Chạy, so sánh kết quả, log bug | | | |
| Completion | Tổng kết, bài học, lưu trữ testware | | | |

**Kết quả:** bảng 7 hoạt động đã điền xong.

---

## Thứ 4 (28/10)

### Tiếng Anh 30'
| Phút | Việc |
|---|---|
| 0-10 | Anki: ôn + học **Bài 3 *Warranties*:** characteristic, consequence, consider, cover, expiration, frequently, imply, promise, protect, reputation, require, variety |
| 10-30 | Chép chính tả (bài mới) |

### Automation 60': L02
| Phút | Việc |
|---|---|
| 0-35 | Xem L02: toán tử `+ - * / %`, prefix/postfix, `printf`, phím tắt IntelliJ, if/else, hằng số, `Scanner` |
| 35-60 | Tự làm (không xem lại video): |

- **Bài 2.1:** nhập 2 số nguyên, in tổng, hiệu, tích, thương và phần dư, dùng `printf`.
- **Bài 2.2:** nhập 1 số, in ra là số chẵn hay lẻ.
- **Bài 2.3 (bài của khóa):** nhập giờ khởi hành và số giờ di chuyển, in giờ đến nơi (gợi ý: dùng `% 24`).
- Đoán trước kết quả rồi mới chạy: `int i = 5; int a = i++ + ++i;` thì `a` = ? và `i` = ?

**Kết quả:** 3 bài đã commit.

---

## Thứ 5 (29/10)

### Tiếng Anh 30'
| Phút | Việc |
|---|---|
| 0-10 | Anki: ôn + học **Bài 4 *Business Planning*:** address, avoid, demonstrate, develop, evaluate, gather, offer, primarily, risk, strategy, strong, substitution |
| 10-30 | Shadowing (cùng đoạn với Thứ 3, mục tiêu đọc nhanh bằng audio) |

### Kiến thức test 60': Testware, traceability, vai trò
| Phút | Việc |
|---|---|
| 0-20 | Đọc: **traceability** là gì (liên kết requirement ↔ test condition ↔ test case ↔ kết quả ↔ bug) và lợi ích của nó (đo coverage, đánh giá ảnh hưởng khi requirement đổi) |
| 20-35 | Đọc: 2 vai trò trong testing (test management role và testing role) và nhiệm vụ của từng vai trò |
| 35-60 | Trả lời bằng ví dụ thật (viết 3-5 dòng mỗi câu): **(a)** Ở dự án bạn, traceability được làm bằng công cụ gì? **(b)** Khi requirement thay đổi, làm sao bạn biết test case nào phải sửa? **(c)** Bạn đảm nhận những nhiệm vụ nào của test management role? |

**Kết quả:** 3 câu trả lời. Đây cũng là nguyên liệu cho phỏng vấn.

---

## Thứ 6 (30/10)

### Tiếng Anh 30'
| Phút | Việc |
|---|---|
| 0-10 | Anki: ôn cả 48 từ |
| 10-30 | **Đọc** 1 bài TOEIC Part 7 ngắn (email/thông báo). Cách làm ở cuối file |

### Phỏng vấn 60': Danh sách dự án
Tạo file `cv/du-an.md`, điền **mọi dự án** trong 8 năm (dự án nhỏ thì gộp lại):

| # | Tên dự án | Thời gian | Domain | Khách hàng (nước) | Vai trò | Team size (QA/tổng) | Loại test | Công cụ | Điểm nổi bật |
|---|---|---|---|---|---|---|---|---|---|
| 1 | | | | | | | | | |

**Gợi ý nhớ lại:** xem lịch sử Redmine/Jira, email, hợp đồng dự án, CV cũ.

**Kết quả:** bảng dự án đầy đủ.

---

## Thứ 7 (31/10)

### Tiếng Anh 30'
| Phút | Việc |
|---|---|
| 0-10 | Anki: ôn thẻ đến hạn |
| 10-30 | Chép chính tả (bài mới) |

### Automation 90': L03 + bài tập
| Phút | Việc |
|---|---|
| 0-45 | Xem L03: for, giá trị `i` sau vòng lặp, vòng lặp vô hạn, mảng 1 chiều, `ArrayIndexOutOfBoundsException`, enhanced for, while |
| 45-90 | Tự làm: |

- **Bài 3.1:** in giá trị max/min của `byte, short, int, long, float, double` (dùng `Integer.MAX_VALUE`...).
- **Bài 3.2:** tính tổng 1 đến n (n nhập từ bàn phím), làm bằng cả for và while.
- **Bài 3.3:** cho mảng `{5, 12, -3, 8, 0, 21}`: tìm max, min, tổng các số chẵn.
- **Bài 3.4:** nhập số đến khi gặp số 0 thì dừng, in tổng (dùng while, vì không biết trước số lần lặp).
- Commit + **push lên GitHub**.

### Kiến thức test 60': SDLC và testing
| Phút | Việc |
|---|---|
| 0-25 | Đọc: mô hình tuần tự (Waterfall, V-model) và lặp/tăng dần (Agile/Scrum). Testing khác nhau thế nào trong từng mô hình. Shift-left |
| 25-60 | Vẽ sơ đồ (giấy hoặc draw.io): **1 sprint/1 release ở dự án của bạn**, ghi rõ ở mỗi bước test process diễn ra hoạt động nào, ai làm, ra testware gì |

**Kết quả:** bài tập đã push. Sơ đồ test process của dự án.

---

## Chủ nhật (01/11)

### Tiếng Anh 30'
| Phút | Việc |
|---|---|
| 0-15 | Ôn 48 từ, đánh dấu những từ hay sai |
| 15-30 | Ghi âm đọc đoạn self-introduction 1 lần, so với bản ghi Thứ 3 |

### Phỏng vấn 60': 5 thành tích theo STAR
Từ bảng dự án hôm Thứ 6, chọn **5 thành tích nổi bật nhất** và viết theo mẫu:

> **S (Situation):** Bối cảnh: dự án gì, vấn đề gì? *(1-2 câu)*
> **T (Task):** Nhiệm vụ của bạn là gì? *(1 câu)*
> **A (Action):** Bạn đã làm cụ thể những gì? *(2-4 ý, dùng "tôi", không dùng "team")*
> **R (Result):** Kết quả **có số liệu**: giảm/tăng bao nhiêu %, tiết kiệm bao nhiêu giờ, bao nhiêu bug *(1-2 câu)*

**Gợi ý chủ đề:** giảm bug leakage, rút ngắn thời gian regression, xây quy trình mới, đào tạo người mới, xử lý release khẩn cấp, cải thiện giao tiếp với khách hàng Nhật.

### Tổng kết tuần 30'
- Điền checklist bên dưới và bảng theo dõi trong [ke-hoach-3-thang.md](../ke-hoach-3-thang.md).
- Phần nào chưa xong thì làm bù luôn trong 30' này.

---

## Cách làm từng kỹ năng tiếng Anh

### Cách làm chép chính tả (20')
1. Chọn bài cấp độ dễ (A1-A2), dài khoảng 30 giây.
2. Nghe từng câu, mỗi câu nghe tối đa 3 lần, rồi gõ lại những gì nghe được (không đoán bừa).
3. Mở transcript, gạch dưới các từ sai hoặc thiếu.
4. Tính **% đúng = số từ đúng / tổng số từ**, ghi vào file theo dõi.
5. Nghe lại toàn bài 1 lần vừa nghe vừa nhìn transcript.

### Cách làm shadowing (20')
1. Đọc to bài 2 lần, tra nghĩa và cách phát âm từ lạ (2').
2. Nghe audio kèm nhìn transcript, nói theo **cùng lúc** với audio, câu ngắn trước (8'). Đoạn trong English/tuan-01.md chưa có audio thì dùng Google Translate hoặc 1 công cụ text-to-speech đọc giúp.
3. Bỏ transcript, chỉ nghe và nói theo (5').
4. Ghi âm lại 1 lần (Thứ 5, Chủ nhật), ghi chú những từ phát âm chưa rõ (5').

### Cách làm đọc (20')
1. Đọc lướt 1 lần lấy ý chính, không tra từ (3').
2. Đọc kỹ, gạch các từ không biết, chỉ tra những từ cản trở việc hiểu (10').
3. Viết **3 ý chính bằng tiếng Việt**, không nhìn lại bài (5').
4. Đưa 2-3 từ mới hay gặp vào Anki (2').

---

## Checklist cuối tuần
- [ ] L01, L02, L03 xong, 7 bài tập đã push lên GitHub
- [ ] Bảng 7 hoạt động test process + sơ đồ áp vào dự án
- [ ] 3 câu trả lời về traceability/vai trò
- [ ] File `cv/du-an.md` + 5 thành tích STAR
- [ ] 48 từ, 3 buổi chép chính tả (ghi %), 2 buổi shadowing, 1 bài đọc
