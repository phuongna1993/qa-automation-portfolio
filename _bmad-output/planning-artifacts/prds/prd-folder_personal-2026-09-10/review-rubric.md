# PRD Quality Review — Hành Trình Mẹ & Bé

No `addendum.md` exists in this PRD's folder (only `prd.md`, `reconcile-brief.md`, `.memlog.md`). `reconcile-brief.md` is a gap-audit against the upstream brief/addendum, not a PRD addendum — its 3 findings have already been patched into `prd.md` (verified below), so it is treated as background, not as review input.

## Overall verdict

This PRD is in good shape for a solo-operator, launch-stakes content strategy: the thesis is coherent, the three UJs are genuinely load-bearing (not decoration), non-goals and assumptions are called out honestly, and the compliance boundary (FR-12–14) is concrete rather than boilerplate. The main risk is a coverage gap, not a quality gap: the UJs and the growth engine stop at "follow / join Group," while the entire revenue thesis (SM-3) depends on what happens after that — a conversion moment the PRD never walks through. A second risk is that one hard business gate (affiliate program eligibility) is stated as descriptive prose instead of being promoted to an enforceable FR the way the structurally similar Group-opening gate (FR-5) was. Neither issue is a rewrite; both are additive fixes.

## Decision-readiness — adequate

Most decisions in this PRD are genuinely decided, not hedged into "considerations" — §8 and `.memlog.md` show real triage (follower-real-vs-bot measurement, Group post-approval, Group-opening threshold, TikTok cadence) with a stated resolution for each, not rhetorical questions answered in the next breath. The two `[NOTE FOR PM]` callouts land on real tensions (SM-3 needs recalibration once real order data exists; outsourcing gets revisited only if revenue hits the 6-month mark) rather than safe checkpoints.

The exception is the affiliate-program eligibility gate. §4.3's opening paragraph states a hard precondition — Shopee requires ≥500 followers (+ KYC), TikTok Shop requires ≥1,000 followers for official Affiliate status — but this is written as descriptive context, not as a decision with a testable consequence. Compare this to FR-5, which promotes a structurally identical gate (Threads follower threshold before the Group can open) to a full FR with its own "Kết quả kiểm chứng được" bullet. The affiliate-eligibility gate is at least as consequential (it blocks FR-8/FR-9/FR-10 monetization outright, and carries a KYC/compliance dimension FR-5 doesn't have), yet it has no equivalent enforcement checkpoint. A reader could satisfy FR-8–FR-10 exactly as written and still be legally/operationally unable to activate them.

### Findings
- **high** Affiliate-eligibility gate stated as prose, not as an enforceable gate (§4.3 intro) — The Shopee (≥500 follower + KYC) and TikTok Shop (≥1.000 follower) preconditions block FR-8/FR-9/FR-10 but exist only as a descriptive paragraph, unlike the parallel Group-opening gate which was promoted to a full FR (FR-5) with a verification bullet. *Fix:* Add a short FR (e.g., FR-16 "Điều kiện đăng ký chương trình affiliate") with its own "Kết quả kiểm chứng được" bullet ("Tài khoản đã đăng ký thành công Shopee Affiliate / TikTok Shop Affiliate (hoặc dùng chia sẻ link ngoài) trước khi FR-8/9/10 được kích hoạt"), and reference it from §6.1 Phase 2/3 gating.

## Substance over theater — strong

No persona theater: the three UJs (Mai, Trang, Hương) are each tied to specific FRs via explicit "Realizes UJ-X" tags and drive genuinely different feature decisions (search-driven discovery → series content; comment-driven discovery → no-link-no-CTA comment policy; knowledge-deep readers → tiered content). No innovation-theater differentiation section was forced in. The Vision (§1) is specific to this creator's actual arc (PCOS → lifestyle → TTC → pregnancy → parenting, across a named 3-channel sequence) rather than swappable wellness-brand boilerplate. The one NFR-shaped item present (§4.4, TikTok content must not be a duplicate template of Threads/Group content, "tránh rủi ro chính sách nội dung AI hàng loạt của TikTok") is grounded in a named platform-policy risk, not generic "must be scalable" language.

No findings — this dimension does not need fixing.

## Strategic coherence — thin (one significant gap)

The thesis is real and consistently applied: authentic first-person PCOS journey content, monetized by staging affiliate links to the reader's life-stage, kept structurally separate from medical claims (FR-14, SM-C2). Feature sequencing follows the thesis (Phase 1 Threads stabilization → Phase 2 Group + PCOS/TTC affiliate → Phase 3 TikTok + pregnancy/postpartum affiliate), not an easy-first backlog order. SM-C1/SM-C2 are real counter-metrics that trade against SM-1/SM-3, which is exactly what this dimension wants to see.

The gap: all three UJs (§2.3) converge on the same endpoint — "follow Threads or join the Facebook Group" — and every FR realization tag (§4.1) stops there too. But the PRD's primary success metric, SM-3 (affiliate revenue), depends entirely on what happens *after* that point: a "follower thật" or Group member encountering a staged affiliate link (FR-8/FR-9) via a bio-link hop (FR-10, needed because Shopee doesn't integrate directly with Threads/TikTok) and actually converting. No UJ walks through this moment. This is the least-proven, highest-uncertainty step in the whole funnel (it's the one place the PRD itself flags unverified assumptions — §9's inherited "audience sẵn sàng mua" assumption), yet it's also the one step with no journey narrative behind it. The PRD is well-formed for growth (top of funnel) and thin for revenue (the metric it's actually staking the "launch-stakes" claim on).

### Findings
- **high** No UJ covers the monetization/conversion moment (§2.3, §4.3) — SM-3 is the PRD's primary success metric, but no UJ traces a Follower-thật or Group member from encountering a staged affiliate link (FR-8/FR-9) through the bio-link hop (FR-10) to a purchase. The three existing UJs all terminate at "follow/join," one step upstream of where the revenue thesis actually lives. *Fix:* Add a fourth UJ (e.g., "Hương thấy link sản phẩm trong bài giai đoạn TTC, bấm bio-link, mua hàng") to pressure-test whether FR-8/9/10 as written actually produce a plausible purchase path, and to give the inherited "audience sẵn sàng mua" assumption something concrete to be checked against.

## Done-ness clarity — adequate

Where verification bullets exist, they are genuinely testable: FR-1's series-labeling and cadence rule, FR-12's disclaimer is a verbatim required string, FR-8/FR-9's product-category boundaries are audit-checkable even without an explicit bullet. But coverage and internal consistency are uneven.

FR-5 states the Group-opening threshold as "≥1.000-1.500 follower" in its own description, then its "Kết quả kiểm chứng được" bullet downgrades the actual enforced floor to "tối thiểu vài trăm follower" (a few hundred) — a materially looser number than the headline figure, for the one FR whose whole job is to gate a phase transition. Separately, 8 of the 15 FRs (FR-6, FR-7, FR-8, FR-9, FR-10, FR-12, FR-13, FR-14) have no explicit "Kết quả kiểm chứng được" block at all, unlike FR-1/2/3/4/5/11/15 — most of these are still self-evidently checkable from the FR text itself (e.g., FR-12's exact disclaimer string), but FR-7 ("lời mời vào nhóm luôn kèm lý do cụ thể") has no concrete bar for what counts as "cụ thể," and would benefit from one.

### Findings
- **medium** FR-5's stated threshold and its own verification bullet disagree (§4.2, FR-5) — Description says "≥1.000-1.500 follower"; the verification bullet says "tối thiểu vài trăm follower" (a few hundred). For the one FR that gates the Phase 1→2 transition, this ambiguity could let the operator open the Group meaningfully earlier or later than intended. *Fix:* Pick one number (or one explicit range with a stated floor) and use it in both places; if "vài trăm" is a deliberate soft floor distinct from the "official" 1.000-1.500 target, say so explicitly.
- **low** FR-3's tiering criterion is a subjective self-check (§4.1, FR-3) — "Có thể phân biệt được (qua tiêu đề/hashtag/series) bài nào thuộc tầng nào khi audit lại" has no concrete rule for what marks a post as "nhập môn" vs "chuyên sâu." *Fix:* Name the actual marking convention (e.g., a fixed hashtag or series-prefix per tier) so the audit has something objective to check against.

## Scope honesty — strong

§5 Non-Goals does real work (no internal tooling, no YouTube channel yet with a named reason tied to brief risk analysis, no second TikTok topic channel, no outsourcing for 6 months, no anonymous identity, no medical-advice positioning) rather than reading as generic disclaimers. §6.2 de-scopes explicitly with reasons, including a `[NOTE FOR PM]` on when outsourcing gets reconsidered. `[ASSUMPTION]` tags are used at genuine points of uncertainty (illustrative UJ names, Google Flow free-tier capacity, Threads Insights as the sole real-follower proxy, blended commission rate) rather than being sprinkled everywhere or nowhere. §8's claim of "no phase-blocking open questions" is credible, not a dodge — `.memlog.md` documents the actual triage that closed each of the four original open questions.

### Findings
- No findings at the scope-honesty level (see Mechanical notes for a smaller assumptions-index roundtrip gap).

## Downstream usability — adequate (matters less; this PRD is standalone)

This PRD explicitly builds no software and feeds no UX/architecture/story-creation pipeline (§0: "Không có phần mềm/công cụ nội bộ nào cần xây"), so strict FR/UJ/SM cross-reference rigor matters less here than in a chain-top PRD. Within that lighter bar: the Glossary (§3) is used consistently for its key terms ("Nhóm," "Giai đoạn PCOS/TTC," "Giai đoạn Mang thai/Sau sinh"), and each UJ has a named protagonist carrying context inline (Mai, Trang, Hương), which is what this dimension is actually checking for in a solo/content shape.

### Findings
- No findings beyond the ID-numbering and glossary-precision items already captured in Mechanical notes.

## Shape fit — strong

This is a single-operator, non-software, launch-stakes-but-solo content and monetization strategy, and the PRD is shaped accordingly: three UJs with named protagonists (appropriate — this is a consumer-facing content product, not an internal tool, so UJs are load-bearing here), FRs that are content/process rules rather than software specs, no forced architecture or security NFR sections, and success metrics that mix audience-growth counts with revenue and two explicit counter-metrics rather than SaaS-style engagement metrics (no DAU/MAU). This is the right level of formality for the stated stakes — not over-built, not hobby-light.

The one place the shape slips is the same gap already flagged under Strategic coherence: the UJ mechanism this PRD correctly chose to use is under-applied exactly where the money is (the affiliate-conversion moment), while it's fully applied where the money isn't (top-of-funnel discovery). That's not a case for more UJs everywhere — it's a case for one more UJ at the highest-stakes point.

### Findings
- No new findings — see Strategic coherence finding above (UJ coverage stops before the monetization moment).

## Mechanical notes

- **ID continuity:** FR-15 ("Duyệt bài trước khi đăng trong Nhóm") sits under §4.2 alongside FR-5/6/7 but is numbered after FR-14, breaking the otherwise sequential FR-1…FR-14 ordering. `.memlog.md` confirms it was added later during gap-triage. Not harmful on its own, but worth renumbering (or footnoting why) before this PRD is used as a source for any downstream tracker.
- **SM traceability gap:** FR-15 is not referenced by any Success Metric or counter-metric ("Kiểm chứng FR-X" in SM-2 lists only FR-5, FR-6, FR-7). Minor, since FR-15 is an always-on operational safeguard rather than a growth lever, but it means there's no stated signal for whether post-approval is actually working as a solo-monitoring substitute.
- **Assumptions Index roundtrip — partial gap:** Of the six items in §9, four have a matching inline `[ASSUMPTION]` tag at the cited location. The last two ("audience giai đoạn PCOS/TTC sẵn sàng mua sản phẩm hỗ trợ lối sống…"; "tăng tần suất và CTA sẽ cải thiện được tỉ lệ follow hiện tại (~0,6%)") are inherited from the brief and indexed in §9, but carry no inline `[ASSUMPTION]` tag anywhere in the PRD body (not in §1 Vision, not in FR-1/FR-4 where CTA and frequency are actually specified). *Fix:* Either add inline tags at FR-4 (CTA) and FR-1 (cadence), or note explicitly in §9 that these two are carried by reference from the brief rather than restated inline.
- **Glossary precision drift:** §3 defines "Follower thật" as a distinct, meaningful term (real vs. bought/bot followers), and SM-1 uses it correctly. But FR-5's threshold and §4.3's Shopee/TikTok Shop eligibility thresholds both just say "follower" without the "thật" qualifier, even though the distinction is exactly what §3 and SM-1 care about. Low stakes given the PRD's own SM-1 assumption that bot-filtering isn't being done anyway, but worth a consistent term choice.
- **Required sections for stakes/type:** Vision, Audience/JTBD, UJs, Glossary, Features/FRs, Non-Goals, Scope-by-phase, Success Metrics (+ counter-metrics), Open Questions, and Assumptions Index are all present — this matches what a solo/launch-stakes, non-software PRD should carry. No addendum was expected or required for this PRD itself (distinct from the upstream brief's own addendum.md, which this PRD correctly declines to duplicate per §0).
