# Rubric Walker Review — ARCHITECTURE-SPINE.md

**Target:** `_bmad-output/planning-artifacts/architecture/architecture-folder_personal-2026-09-10/ARCHITECTURE-SPINE.md`
**Driving spec:** `_bmad-output/planning-artifacts/prds/prd-folder_personal-2026-09-10/prd.md` (16 FRs, 5 features)
**Checklist source:** `.claude/skills/bmad-architecture/references/reviewer-gate.md`, "Good-spine checklist" (line 11)
**Nature of artifact:** not software — a consistency spine for a solo-operator, multi-channel content/affiliate strategy (Threads → Facebook Group → TikTok), with a cross-cutting Compliance filter. Evaluated against the checklist's intent (divergence points between "units" = channels/stages), not literal code/deploy language.

## Verdict

Conditional pass — the spine's shape and channel/stage-boundary ADs are sound and cover the PRD's capability surface, but it silently under-specifies the operational envelope (platform outage/ban and policy-change response) and has one enforceability gap and one real, named divergence point (TikTok content duplication) that slipped through without a governing rule.

---

## Checklist item-by-item

### 1. Fixes the real divergence points for the level below, misses none

Mostly yes. The five ADs correctly capture the load-bearing divergence points implied by the PRD: stage-vs-affiliate-type boundary (AD-1), compliance as cross-cutting rather than per-channel (AD-2), a single hashtag taxonomy across channels (AD-3), stage-gates as the sole trigger for channel/monetization expansion (AD-4), and narrative/commercial post separation (AD-5). These map cleanly onto the PRD's actual stated risks (FR-8/9 boundary, FR-12/13 cross-channel compliance, FR-3 taxonomy, FR-5/16 gating, FR-14 separation).

One real divergence point named explicitly in the PRD is **not** covered by any AD or Convention: FR-11's feature-specific NFR states TikTok content "không được là bản sao/template trùng lặp của nội dung trên kênh Threads/Nhóm — tránh rủi ro chính sách nội dung AI hàng loạt của TikTok." This is exactly the shape of thing the spine exists to prevent — a new channel (TikTok) drifting out of consistency with (or here, into over-identical copying of) the established channels — yet neither an AD nor the Consistency Conventions table addresses how TikTok content is required to differ from/adapt versus Threads/Group source material. See Finding 3.

### 2. Every AD's Rule is enforceable and actually prevents its stated divergence

Four of five hold up. AD-2, AD-3, AD-4, AD-5 each give an auditable test (checklist before posting; hashtag namespace; numeric follower thresholds; narrative-post-has-no-link vs commercial-post-has-link-no-efficacy-claim).

AD-1 does not fully hold up. Its Rule is stated as bidirectional — PCOS/TTC-tagged content must not carry mẹ-&-bé affiliate, **and** "ngược lại nội dung giai đoạn Mang thai/Sau sinh không gắn affiliate hỗ trợ lối sống giai đoạn PCOS/TTC." The forward direction is mechanically checkable via the `#PCOS101`/`#PCOSTTC` hashtags (AD-3). The reverse direction has no equivalent marker: no hashtag/namespace is defined anywhere in the spine (or the PRD) for "giai đoạn Mang thai/Sau sinh" content, so there is no way to mechanically identify which posts that half of the rule even applies to. See Finding 2.

### 3. Nothing under Deferred could let two units diverge

Clean. All four Deferred items (YouTube channel, other TikTok topic channels, collaborator onboarding, bio-link/tracking tooling) are things that are not yet active, and two of them explicitly flag that a *new* AD will be needed before they go live (TikTok topic-channel duplication risk; AD-2 needing a stronger enforcement mechanism once collaborators exist). No live divergence risk is parked here.

### 4. Named tech is verified-current

No issue found. Threads, Facebook Groups, TikTok, Shopee Affiliate, TikTok Shop Affiliate, Claude Team, Gemini, and Google Flow are all current, real platforms/tools. The two genuinely unverified items (Google Flow free-tier capacity; which bio-link tool) are honestly flagged inline as `[ASSUMPTION]` rather than stated as settled fact — correct handling, not a finding.

### 5. Ratifies rather than contradicts a brownfield codebase

Not applicable — this is a greenfield spine; there is no prior codebase/strategy artifact it must ratify.

### 6. Covers the driving spec's capabilities

Yes. The Capability → Architecture Map row-for-row covers all five PRD features and all 16 FRs (FR-1 through FR-16, no gaps, no phantom FRs). Front-matter `binds: ['FR-1..FR-16']` matches the PRD's FR range exactly.

One accuracy nit inside this otherwise-complete map: FR-15 (Group post pre-approval) is listed as "Governed by: AD-2, AD-4," but neither AD's Rule text actually says anything about member-post moderation — AD-2 is the operator's own pre-publish compliance checklist, AD-4 is stage-gate thresholds. The mapping cell looks filled-in for completeness rather than because either AD constrains FR-15. See Finding 4.

### 7. No new AD weakens or contradicts an inherited parent AD

Not applicable — `companions: []`, no parent spine.

### 8. Every dimension the altitude owns is decided/deferred/open — especially the operational/environmental envelope

This is where the spine is weakest. For a solo-operator, platform-dependent strategy, the operational envelope reduces to three concrete questions:

- **Who/what enforces the rules day-to-day, given one operator?** — Adequately handled. AD-2's Rule is the enforcement mechanism (a pre-publish checklist), and the Deferred section explicitly names the current mechanism as self-discipline ("tự giác") and states what will need to change ("AD-2 sẽ cần một cơ chế thực thi mạnh hơn") once collaborators exist. Decided + forward-looking deferral with a stated trigger. No finding.

- **What happens when a platform changes its policy or algorithm?** — Not decided, not deferred with a stated reason, not logged as an open question. The only trace is a passing remark in an HTML comment above the "Nền tảng & Công cụ" table: "thay đổi chính sách/gói của các nền tảng này là rủi ro ngoài tầm kiểm soát, ghi nhận ở đây để biết khi nào cần rà lại spine." This acknowledges the risk category exists but commits to nothing — no review cadence, no trigger condition, no fallback behavior, and it isn't a Deferred bullet or Open Question the way the spine treats its other known-unknowns. Given that the PRD's own addendum explicitly flags TikTok's AI-content policy risk and Meta/FTC disclosure requirements as live concerns, this reads as the "domain-focused draft skips the operational envelope" case the checklist warns about. See Finding 1.

- **What happens on platform outage/ban (account suspension, Group takedown, TikTok ban)?** — Silently missing entirely. There is no AD, Convention, Deferred bullet, or Open Question anywhere in the spine addressing account loss/suspension on any of the three platforms, despite the whole funnel (Threads growth → owned Group → TikTok) being single-account-per-platform with no stated backup/export/continuity mechanism (e.g., an owned email/contact list independent of platform accounts). This is the single most consequential gap: a Threads ban would sever the top of the funnel with no documented fallback. See Finding 1.

---

## Findings (tiered)

**High**

1. **Operational envelope silently under-addressed: platform outage/ban and policy-change response.** No AD, Deferred entry, or Open Question covers (a) what happens if the Threads/Group/TikTok account is banned or suspended, or (b) how the strategy responds to a platform policy/algorithm change beyond a one-line caveat in a table comment. Given the entire funnel depends on account continuity on three platforms with explicitly flagged policy risk (medical claims, AI-generated content), this should at minimum be a named Deferred item with a stated reason ("out of scope for a solo-operator v1, revisit if X happens") or an Open Question — not silent. *Disposition: discuss with user; likely add as a Deferred item with an explicit trigger (e.g., "no backup/continuity plan for account loss; accepted risk for v1, revisit if an account is suspended or before scaling paid spend") rather than leaving it unaddressed.*

**Medium**

2. **AD-1's Rule is only enforceable in one direction.** The reverse-direction clause ("nội dung giai đoạn Mang thai/Sau sinh không gắn affiliate hỗ trợ lối sống giai đoạn PCOS/TTC") has no namespace/hashtag identifying "giai đoạn Mang thai/Sau sinh" content, unlike the forward direction which relies on AD-3's `#PCOS101`/`#PCOSTTC`. As written, an auditor cannot mechanically check the reverse half of the rule. *Disposition: autofix-able — either extend AD-3's namespace to tag the later-stage content too, or narrow AD-1's Rule to state it's enforced by exclusion (absence of PCOS/TTC hashtags) rather than by a positive marker.*

3. **A named cross-channel divergence point has no governing AD or Convention.** PRD FR-11 explicitly flags the risk of TikTok content being a duplicate/template copy of Threads/Group content (tied to TikTok's AI-content policy risk in the addendum), but the spine has no rule constraining how TikTok content must be adapted/differentiated from source material on the other channels. *Disposition: discuss — likely a 6th AD ("TikTok content must be substantively adapted, not reformatted, from Threads/Group source material") or an addition to the Consistency Conventions table.*

**Low**

4. **Capability map governance mismatch for FR-15.** The Capability → Architecture Map lists FR-15 (Group post pre-approval) as "Governed by: AD-2, AD-4," but neither AD's Rule text addresses member-post moderation. The cell appears to have been filled in for table completeness rather than reflecting an actual constraining rule. *Disposition: either add a short AD/Convention for moderation posture, or change the cell to indicate FR-15 is a direct PRD requirement with no AD governance needed (not every FR requires one).*

5. **AD-1's Binds field over-claims scope.** AD-1 lists `Binds: FR-8, FR-9, FR-14`, but FR-14 (narrative/commercial separation) is actually enforced by AD-5's Rule, not AD-1's (AD-1's Rule concerns stage-crossing product types, not post-structure separation). Minor accuracy issue in the Binds metadata; doesn't affect actual coverage since AD-5 also (correctly) binds FR-14. *Disposition: autofix — drop FR-14 from AD-1's Binds list.*

---

## Not-applicable checklist items

- "Ratifies rather than contradicts a brownfield codebase" — no existing codebase/prior strategy artifact; greenfield spine.
- "No new AD weakens or contradicts an inherited parent AD" — no parent spine (`companions: []`).
