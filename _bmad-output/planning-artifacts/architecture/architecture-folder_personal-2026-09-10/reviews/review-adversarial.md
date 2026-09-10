---
type: architecture-review
lens: adversarial
target: ARCHITECTURE-SPINE.md (Hành Trình Mẹ & Bé — Consistency Spine)
reviewed: 2026-09-10
method: >
  For each AD, construct two (or more) concrete outputs — from two people, the same
  operator on two days, or the operator vs. an AI content tool — that each satisfy the
  AD's literal rule text, and check whether they nonetheless collide, contradict, or
  read as different policies. A finding only counts if both sides can defend their
  choice by quoting the spine, not by "obviously breaking the rule."
---

# Adversarial Review — Hành Trình Mẹ & Bé Consistency Spine

## Verdict

The spine's five ADs are individually well-formed, but four of them leave the exact
kind of interpretive gap they were written to close, and the Capability→Architecture
Map contains a direct, citable self-contradiction about which channels AD-5 governs.
Two operators (or the operator + an AI tool) can each quote an AD verbatim and still
ship incompatible content. Ranked findings below.

## Summary Table

| # | Severity | Finding |
| --- | --- | --- |
| 1 | Critical | Capability Map contradicts itself on whether AD-5 (narrative/commercial separation) covers TikTok at all |
| 2 | High | AD-1 and AD-5 don't get the "new channel will assume this is someone else's rule" patch that AD-2 explicitly got — TikTok can legally mix stages and fuse narrative+commercial |
| 3 | High | AD-4's stage-gate has two numbers-only thresholds and one vague one ("nhịp ổn định, Phase 3"), directly undercutting AD-4's own claim to be "điều kiện duy nhất" |
| 4 | High | AD-4's "TikTok Shop ≥1.000 follower" doesn't name which platform's follower count — two defensible readings give wildly different launch dates |
| 5 | Medium-High | AD-3 gives a namespace (2 hashtags) but no classification rule for "nhập môn" vs "chuyên sâu" — same topic can be tagged either way |
| 6 | Medium-High | AD-2's disclaimer/disclosure text is "nguyên văn"/"kiểu" (illustrative, not verbatim-mandatory) with no placement, prominence, or modality (text vs. spoken video) rule |
| 7 | Medium | AD-5 mandates "two separate posts" but not independence between them — same-thread reply-chains can recreate the exact fusion it bans |
| 8 | Medium | AD-1's stage boundary is hashtag-driven and self-referential; non-PCOS stages (Mang thai/Sau sinh) have no namespace at all, so "which stage is this post" has no independent test |

---

## Finding 1 (Critical) — AD-5's channel scope contradicts itself inside the same table

**Where:** Capability → Architecture Map, two rows:

> `Cơ chế kiếm tiền theo giai đoạn (FR-8, FR-9, FR-10, FR-16) | Nhóm Facebook + bio-link | AD-1, AD-4, AD-5`
>
> `Tuân thủ & niềm tin (FR-12..FR-14) | Xuyên suốt mọi kênh | AD-2, AD-5`

AD-5's own header says `Binds: FR-14`. FR-14 appears only in the second row, whose
"Lives in" column is **"Xuyên suốt mọi kênh"** (all channels, including TikTok). The
first row also lists AD-5 as a governor, but its "Lives in" column is **"Nhóm Facebook
+ bio-link"** — explicitly not TikTok.

**Scenario:** The operator ships a TikTok video that opens with a personal PCOS
recovery story and closes the same video with a Shopee-affiliate product link and a
mild efficacy framing ("sản phẩm này đã giúp mình rất nhiều"). Auditor A pulls up the
Capability Map, reads FR-14's row ("Xuyên suốt mọi kênh, AD-2, AD-5"), and flags a
violation: narrative and commercial content were fused in one artifact, which is
exactly what AD-5 exists to prevent. Auditor B pulls up the TikTok row ("Mở rộng
TikTok (FR-11) | TikTok | AD-2, AD-3") — AD-5 isn't listed as governing TikTok at
all — and the monetization row's own "Lives in" column ("Nhóm Facebook + bio-link")
that does carry AD-5 explicitly excludes TikTok. Auditor B closes the ticket: no rule
was broken, because per the map's own scoping, AD-5 doesn't reach TikTok.

Both auditors are quoting the same document correctly. The map cannot simultaneously
mean "AD-5 is Facebook/bio-link-only" and "AD-5 is cross-channel," but it says both.

**Fix:** Pick one. If AD-5 is meant to be cross-cutting like AD-2 (which is almost
certainly the intent, since narrative/commercial fusion is just as possible in a TikTok
video as in a Facebook post), say so explicitly in AD-5's own rule text — the way AD-2
does ("áp dụng độc lập ở mọi filter") — not only implicitly via one ambiguous map row.
Then make every row in the Capability Map that touches FR-14 or FR-8/9/10/16 agree.

---

## Finding 2 (High) — AD-1 and AD-5 lack the exact patch AD-2 gave itself against "new channel thinks this is someone else's rule"

AD-2's own **Prevents** clause names the failure mode directly:

> "Kênh mới (TikTok, hoặc kênh tương lai) bỏ sót disclaimer/disclosure vì hiểu nhầm đó
> là 'quy tắc riêng của Threads.'"

The spine's authors clearly anticipated that a channel-scoped Capability Map would be
misread as "this AD only applies where the map says it lives," and wrote AD-2's rule
text to override that misreading for compliance specifically ("áp dụng độc lập ở mọi
filter, không phụ thuộc filter nào đứng trước").

Neither AD-1 nor AD-5 got the same override. Their rule text is written in generic
terms ("Mỗi bài chỉ thuộc đúng một giai đoạn," "Bài chia sẻ trải nghiệm cá nhân...luôn
là hai bài tách biệt") with no explicit "this applies on every channel regardless of
what the map says" clause — and the Capability Map (per Finding 1) actively scopes
AD-1 and AD-5 to "Nhóm Facebook + bio-link," not TikTok.

**Scenario:** The operator (or an AI content tool briefed only with "follow AD-3 and
AD-2 for TikTok" — the two ADs the map actually lists for the TikTok row) produces a
TikTok video that tags `#PCOS101` and, in the same video, promotes a baby-care
affiliate product — the exact cross-stage mixing AD-1 forbids on Facebook. Checked
against the TikTok row of the Capability Map, this is fully compliant: AD-1 isn't
listed as governing that capability. The same content posted to the Facebook Group
would be a clear AD-1 violation. Two channels, same content, opposite verdicts — not
because anyone broke a rule, but because the map only wired the stage-boundary and
narrative/commercial rules to one channel.

**Fix:** Either (a) restate AD-1 and AD-5 with an explicit "applies on every channel"
clause mirroring AD-2's, or (b) if the Capability Map's channel column is meant to be
purely descriptive ("primarily relevant to") rather than scoping, say that once at the
top of the map — right now a literal reader has no way to tell which reading is
correct, and the AD-2 precedent suggests the authors themselves treat it as scoping.

---

## Finding 3 (High) — The stage-gate chain has a numeric gate, a numeric gate, and a vibe

AD-4's rule text: "Chỉ mở Nhóm khi Threads ≥1.000 follower thật; chỉ đăng ký affiliate
khi đạt ngưỡng chương trình tương ứng." Both examples given are hard numbers. But the
diagram right below AD-5 shows the *next* transition differently:

> `B -->|"nhịp ổn định, Phase 3"| C`  (Nhóm → TikTok)

"Nhịp ổn định" (a stable posting rhythm) is not a threshold — it's a judgment call, and
AD-4 claims to be "**điều kiện duy nhất**" (the *only* condition) for opening a new
channel or activating affiliate. If the only condition for Group→TikTok really is
"nhịp ổn định," that condition needs the same rigor AD-4 gives the Threads→Group gate;
if it's actually still a follower/time threshold, the diagram is describing a
different, undocumented gate that AD-4's rule text never states.

**Scenario:** Operator A (disciplined reading of AD-4) refuses to open TikTok until
they can point to a number — say, 12 consecutive weeks of on-schedule Group posts with
zero missed days — and treats anything less as "not actually a stage-gate, just a
feeling," consistent with AD-4's demand for an objective, non-cảm-tính condition.
Operator B, working from the diagram's literal label, opens TikTok the first month
that "feels" consistent (four posts in four weeks, one of which was two days late) and
calls it "nhịp ổn định" — also a literal reading of the only text that actually names
the Group→TikTok gate. Both can cite the spine. Their launch dates could differ by
months.

**Fix:** Give the Group→TikTok transition the same treatment as the other two gates —
either a concrete metric (weeks of on-schedule posting, minimum post count, minimum
engagement) or an explicit statement that this transition is deliberately
judgment-based and therefore *not* covered by AD-4's "điều kiện duy nhất" claim (in
which case the diagram edge label and AD-4's rule text need to stop implying they're
the same kind of gate).

---

## Finding 4 (High) — "TikTok Shop ≥1.000 follower" doesn't say on which platform

AD-4: "...TikTok Shop ≥1.000 follower." Threads is the only channel active before
Phase 3, and the Threads→Group gate is also phrased as "≥1.000 follower" — on Threads.
Nothing in AD-4, the table, or the map states whether the TikTok Shop threshold is
measured on the (not-yet-launched) TikTok channel itself, or is the same Threads
count reused as a blanket "you've proven you can grow an audience" gate that also
unlocks TikTok Shop registration.

**Scenario:** Operator A treats the number as native to the program it names (a
"TikTok Shop" threshold is naturally read against TikTok followers) and won't
register until the brand-new TikTok channel itself hits 1,000 followers — potentially
months after Threads passed 1,000. Operator B notes that AD-4's own two examples in
the same sentence are both phrased identically ("≥1.000 follower") with only Shopee's
explicitly anchored to Threads ("Shopee ≥500 follower Threads" is how it's used
elsewhere in the doc), and reads the TikTok Shop number as reusing whatever count is
current at the time — i.e., registers for TikTok Shop the moment Threads crosses 1,000,
before a single TikTok video is posted. Both are defensible readings of the same
clause; the resulting registration dates could be a year apart, and one of the two
readings has the operator registering for a TikTok-specific commission program with
zero TikTok presence.

**Fix:** Name the platform explicitly for every threshold in AD-4 ("Threads ≥1.000",
"Shopee: Threads ≥500", "TikTok Shop: TikTok ≥1.000" or whatever was actually decided)
rather than relying on "follower" as an unqualified noun across three different
channels in one sentence.

---

## Finding 5 (Medium-High) — "Nhập môn" vs "chuyên sâu" has no test, so the same topic can get either tag

AD-3 fixes the *names* (`#PCOS101`, `#PCOSTTC`) but not the *classification rule*
between them — "nhập môn" (introductory) and "chuyên sâu" (in-depth) are relative,
audience-dependent labels with no stated criterion (reading level? topic list?
whether it assumes prior posts? whether it discusses medication/lab values?).

**Scenario:** Both the operator and an AI drafting tool are asked to write a post
explaining insulin resistance in PCOS in accessible language, covering what it is and
why it matters for TTC. The operator classifies it `#PCOS101` — reasoning: it's
explaining a concept from scratch, in plain language, for someone new to PCOS. The AI
tool, briefed with "TTC content should carry the TTC tag," classifies structurally
identical output `#PCOSTTC` — reasoning: insulin resistance is specifically relevant
to trying-to-conceive readers, which per the doc is the "chuyên sâu" track. Both
outputs satisfy AD-3's literal rule ("dùng đúng namespace, không tạo hashtag mới") —
neither invented an alternate tag — yet a reader following `#PCOS101` for beginner
content and skipping `#PCOSTTC` as "not ready for that yet" gets inconsistent
signal about where to find (or avoid) the same information depending on who tagged
it that day. This directly undermines AD-3's stated purpose: a single, predictable
taxonomy readers can rely on across channels.

Compounding this: AD-1 keys its affiliate stage-boundary check off *this same tag*
("Bài gắn hashtag #PCOS101/#PCOSTTC...không được gắn affiliate đồ mẹ & bé"). So the
101-vs-TTC ambiguity doesn't just cause reader confusion — it silently changes which
posts AD-1 treats as PCOS-stage vs. eligible-for-baby-affiliate, without anyone
intending a stage-boundary decision at all.

**Fix:** Add a short, checkable rule distinguishing the two tags — e.g., by content
type (symptom/definition/lifestyle-basics → 101; diagnostics, treatment protocols,
TTC-specific medical detail → TTC) or by series position (first N posts of any topic
→ 101, follow-ups → TTC) — anything that removes the judgment call, since AD-1 now
silently depends on it.

---

## Finding 6 (Medium-High) — Disclaimer/disclosure text is illustrative, not verbatim, and has no placement or modality rule

The Consistency Conventions table gives the compliance wording as: "Disclaimer
**nguyên văn**: 'đây là trải nghiệm cá nhân, không thay thế tư vấn bác sĩ'. Disclosure
**nguyên văn kiểu** '#quảngcáo' / 'link tiếp thị liên kết'." "Nguyên văn" (verbatim)
is claimed for the disclaimer, but the disclosure line hedges with "kiểu" (something
*in that style*), and AD-2's actual rule (the enforceable AD, not the convention table)
only tests presence: "có trải nghiệm cá nhân → có disclaimer; có affiliate link → có
disclosure." Nothing governs *where* in the post it sits, how prominent it must be, or
what "có" means for a video/audio post.

**Scenario A (wording drift):** Operator posts A includes the exact sentence,
bolded, as the first line of a Threads post. An AI drafting tool, generating a
different post, produces "mình chia sẻ theo kinh nghiệm bản thân thôi nha, không phải
lời khuyên y khoa, mọi người vẫn nên hỏi bác sĩ nhé" — same meaning, friendlier tone,
not the verbatim string — and buries it as the last line after four paragraphs. Both
posts pass AD-2's actual test ("có disclaimer": yes) since AD-2 doesn't require
"nguyên văn" itself (only the convention table's aspirational phrasing does, and even
that only binds the disclaimer, not the disclosure). A reader scrolling both posts
would not recognize them as following the same policy — one reads as a prominent,
standardized warning; the other reads as a casual, easy-to-miss aside.

**Scenario B (modality — TikTok):** One TikTok video speaks the disclaimer aloud but
never writes it in the caption. Another only puts it in the on-screen caption text
and never says it aloud. Both "have" a disclaimer somewhere in the artifact. A viewer
watching with sound off (extremely common on the platform) sees the disclaimer in the
second video and never encounters it in the first; the reverse for a viewer who
listens but doesn't read captions. AD-2's channel-agnostic "có disclaimer" test has no
way to distinguish these, even though the operator's actual compliance exposure
(a viewer never seeing the warning) differs sharply between them.

**Fix:** Promote "nguyên văn" (or an approved short list of equivalent phrasings) from
the Conventions table into AD-2's enforceable rule text itself, and add: (a) a
placement rule (e.g., "trong 2 dòng đầu / trong 5 giây đầu video," not "somewhere in
the post"), and (b) a modality rule for video (must appear in *both* on-screen text
and spoken/caption-track, not either/or).

---

## Finding 7 (Medium) — "Hai bài tách biệt" doesn't define independence, so a reply-chain can re-fuse them

AD-5 requires narrative and commercial content to be "luôn là hai bài tách biệt" (two
separate posts) but says nothing about timing, sequencing, or cross-referencing
between them.

**Scenario:** Operator A posts the personal-experience story on Monday with no link,
and — unrelated in time, framing, and thread — posts a product post about a
lifestyle-support item three weeks later with no reference back to the story. Operator
B posts the personal-experience story, then immediately (same day) replies to their
own post, in the same thread, with: "Sản phẩm mình vừa kể ở trên, mọi người có thể
tham khảo tại đây [link] — #quảngcáo." Both operators produced literally two separate
posts (two distinct post objects, satisfying AD-5's countable rule), but B's
reply-chain reconstructs exactly the fused narrative-plus-efficacy-implying-commercial
read AD-5 exists to prevent — a reader encounters both in one scroll, explicitly
linked by "sản phẩm mình vừa kể," with the same net effect as one merged post.

**Fix:** Add a minimum-independence rule to AD-5 — e.g., no same-thread reply linking
the two, no explicit cross-reference ("sản phẩm mình vừa kể") within N days, or a
minimum time/post gap between a stage-relevant narrative post and any commercial post
that could be read as its sequel.

---

## Finding 8 (Medium) — Stage classification is hashtag-driven and self-referential; non-PCOS stages have no namespace

AD-1 tests stage membership by checking whether a post carries the PCOS hashtags
(AD-3's namespace), not by any independent definition of "this post is PCOS-stage
content." AD-3 itself only defines a namespace for the PCOS stage — "Mang thai" and
"Sau sinh" stages, referenced directly in AD-1's own rule text, have no hashtag or
taxonomy defined anywhere in the spine.

**Scenario:** A post discusses managing PCOS symptoms during early pregnancy after a
TTC journey — content that is simultaneously about PCOS and about being pregnant.
Operator A tags it `#PCOSTTC` (it's about the PCOS/TTC condition) and, per AD-1,
withholds baby-care affiliate links. Operator B, focused on the pregnancy angle,
doesn't apply either PCOS hashtag at all (arguing the post has "moved on" to the
Mang thai stage, which per AD-1's own text is a distinct, ungoverned-by-hashtag
category) and freely attaches a baby-care affiliate link to the same underlying
content. Neither operator technically violates AD-1's rule as written ("bài gắn
hashtag PCOS...không gắn affiliate mẹ & bé" — B's post simply isn't tagged, so the
rule's trigger condition never fires), yet the two treatments of equivalent content
are opposite, and the AD offers no independent stage test to arbitrate.

**Fix:** Define stage membership by content criteria first (a short decision rule:
what topics/keywords put a post in PCOS/TTC vs. Mang thai vs. Sau sinh), and treat the
hashtag as a *label applied after* that classification, not the classification
mechanism itself. Also give Mang thai/Sau sinh their own namespace entries in AD-3 so
AD-1 has something concrete to check against for every stage, not just PCOS.

---

## Not included as findings (considered, judged too weak to count as genuine collisions)

- Hashtags behaving differently across platforms (clickable/searchable on Threads and
  TikTok, likely inert in a Facebook Group) — a real UX inconsistency, but doesn't
  produce two *contradictory compliant outputs*, just a weaker experience on one
  channel. Worth a note if the spine is revised, not a hole in the AD itself.
- "Follower thật" (real followers) having no verification method — flagged as an
  aggravating factor inside Finding 3/4 rather than its own finding, since it compounds
  an already-identified ambiguity rather than creating an independent one.
