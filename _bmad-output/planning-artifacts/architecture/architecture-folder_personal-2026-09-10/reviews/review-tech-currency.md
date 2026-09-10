# Tech-Currency Review — ARCHITECTURE-SPINE.md ("Nền tảng & Công cụ")

**Reviewed file:** `_bmad-output/planning-artifacts/architecture/architecture-folder_personal-2026-09-10/ARCHITECTURE-SPINE.md`
**Review date:** 2026-09-10
**Method:** WebSearch (mostly returned "tool unavailable" — see Verification Log) + WebFetch against vendor/reference pages, cross-checked line by line against the "Nền tảng & Công cụ" table and the follower-threshold claim in AD-4.

## Verdict

Most named platforms check out as current and correctly named, but two committed numeric thresholds that gate a real architecture decision (AD-4) and the "solo operator fits the Claude Team plan" implication were never actually confirmed against the web before being written down as settled facts — they need an `[ASSUMPTION]`/`[UNVERIFIED]` tag and a pre-launch recheck, not silent trust.

## Findings (most severe first)

### 1. HIGH — Shopee ≥500 follower / TikTok Shop ≥1.000 follower thresholds are unverified, uncontested, and untagged
- **Location:** AD-4 rule text (line 48): *"chỉ đăng ký affiliate khi đạt ngưỡng chương trình tương ứng (Shopee ≥500 follower, TikTok Shop ≥1.000 follower)"*. Also implicitly the "Shopee Affiliate" / "TikTok Shop Affiliate" rows in the Nền tảng & Công cụ table (lines 86-87), which carry no confidence tag at all.
- **What I found:** I could not confirm these two numbers. WebSearch was unavailable for effectively every query I ran this session (Shopee and TikTok Shop threshold queries included — see log below); the one query that did succeed (Threads status) was pure luck early in the session. WebFetch against `affiliate.shopee.vn` and TikTok's affiliate/creator pages returned only a page `<title>` — both are JS-rendered SPAs with no eligibility text reachable by a static fetch.
- **Why it matters:** These two numbers are exactly the kind of externally-owned, frequently-changing fact the doc's own comment on the table warns about ("thay đổi chính sách/gói của các nền tảng này là rủi ro ngoài tầm kiểm soát"). Real-world affiliate programs (Shopee's and TikTok Shop's own creator/affiliate onboarding rules) are known to change follower/eligibility minimums by market and over time, and criteria differ by category and sometimes bypass follower count entirely in favor of engagement/verification-based approval. Unlike the bio-link tool line, which is honestly marked `[ASSUMPTION]`, these thresholds are stated as settled fact and used to gate a hard architecture rule (AD-4) — if either number is stale, the operator could either register too early (rejected, wasted effort/reputation) or delay registration for months waiting to clear a bar that no longer applies.
- **Recommendation:** Tag both numbers `[ASSUMPTION — chưa xác nhận qua nguồn hiện hành, cần Shopee/TikTok Shop kiểm tra trực tiếp trước khi đăng ký]` and add a note to re-verify on Shopee's/TikTok Shop's own affiliate onboarding page at the moment the operator is about to hit each threshold (not now, since these terms can drift months out).

### 2. MEDIUM — "Claude Team" may not be the right-fit plan for a solo operator (unverified fit, not unverified existence)
- **Location:** Nền tảng & Công cụ table, line 88: `Claude Team, Gemini | Soạn kịch bản/nội dung (Threads, TikTok)`.
- **What I found (confirmed via WebFetch of claude.com/pricing):** Claude Team is a real, current plan — "for teams of 2 to 150," Standard seat $20/mo (annual) or $25/mo (monthly), Premium seat $100/$125. The plan is architected around multi-seat billing/admin (SSO, central billing, seat mixing), not a single-person use case.
- **Why it matters:** The spine names "Claude Team" specifically (not "Claude Pro," which is Anthropic's individual-user tier) for a strategy explicitly described as one person operating solo for at least 6 months (see Deferred section, line 106: "vận hành một mình trong 6 tháng đầu"). It's unclear whether this was a deliberate choice (e.g., wanting Team-only features) or an unverified/incorrect plan name where "Claude Pro" was actually meant. This wasn't reality-checked against fit for a 1-person operation.
- **Recommendation:** Confirm intent — if the operator is truly solo, verify whether Claude Pro is sufficient/cheaper, or whether a specific Team-only feature (e.g., higher usage caps) is the actual reason for choosing Team despite the multi-seat framing.

### 3. LOW — Google Flow: name and free tier are current and real, but the doc's own caveat undersells a second, more concrete risk
- **Location:** Line 89: `Google Flow (free tier) | ... — [ASSUMPTION] free tier đủ dùng, chưa kiểm chứng`.
- **What I found (confirmed via WebFetch of labs.google):** "Google Flow" is the correct, current name for Google's AI video/image creative studio (built on Veo 3.1, "Nano Banana," and Gemini). It does have a genuine free tier — Google-account holders get 50 daily Flow credits at no cost, with paid Google AI Plus/Pro/Ultra tiers unlocking more. So the product name and free-tier claim are both accurate — good, this line was evidently reality-checked correctly (or gotten right by chance) and is honestly flagged as unverified-for-sufficiency, which is the correct move.
- **Additional risk not mentioned in the doc:** Flow's terms restrict it to users 18+ in select regions, and availability/credit limits can vary by country. Since this is a Vietnam-based solo operation, it's worth the operator explicitly confirming Flow is available (and the credit math still works) from a Vietnamese Google account, not just generically "the free tier exists."
- **Recommendation:** No name/product-existence problem here. Optionally extend the existing `[ASSUMPTION]` note to also cover regional availability, not just quota sufficiency.

### 4. INFO — Threads, Facebook Groups, TikTok, Gemini: current and correctly named, no red flags found
- **Threads** (confirmed via WebSearch): active, ~500M MAU as of mid-2026, Meta has stated no plans to shut it down or introduce ads until 1B MAU. Feature fits as described (growth-engine channel).
- **TikTok** (confirmed via WebFetch of Wikipedia): remains operational in most countries; Vietnam is not among the countries currently subject to bans/restrictions (India, Afghanistan, Albania, Canada, EU, US are the ones listed) — no indication TikTok itself is at risk for this Vietnam-based plan.
- **Gemini** (confirmed via WebFetch of Wikipedia): actively maintained, with model releases through mid-2026 (Gemini 3.1 Pro, 3.6 Flash), broad deployment across 239 countries/regions — current and real.
- **Facebook Groups**: not independently re-verified this session (WebSearch was down for this query), but it is a decade-plus-old, still-core Meta product feature; risk of it having been discontinued or renamed is negligible. Flagging only for completeness — not a finding requiring action.

## Verification Log (for auditability)

| Claim | Method | Result |
| --- | --- | --- |
| Threads still active/current in 2026 | WebSearch | Confirmed — 500M MAU, no shutdown planned |
| Google Flow real product name + free tier | WebFetch `labs.google/flow/about` | Confirmed — real name, free tier = 50 daily credits |
| Claude Team plan exists/current pricing | WebFetch `claude.com/pricing` (redirected from anthropic.com/pricing) | Confirmed — $20-25 (standard) / $100-125 (premium) per seat/mo, "for teams of 2 to 150" |
| Gemini still active/current in 2026 | WebFetch `en.wikipedia.org/wiki/Google_Gemini` | Confirmed — active through mid-2026 releases |
| TikTok operational status, incl. Vietnam | WebFetch `en.wikipedia.org/wiki/TikTok` | Confirmed operational; Vietnam not in restricted-country list |
| Shopee Affiliate ≥500 follower threshold | WebSearch (7+ attempts, all query phrasings) + WebFetch (`affiliate.shopee.vn`, Bing search) | **Not verified** — WebSearch tool returned "unavailable" on every attempt after the first lucky hit; WebFetch got only a page `<title>`, no eligibility content (JS-rendered page) |
| TikTok Shop Affiliate ≥1.000 follower threshold | WebSearch (5+ attempts) + WebFetch (`shopaffiliate.tiktok.com` — DNS failure; Bing search) | **Not verified** — same tool-availability problem; no reachable static content with the actual number |
| Facebook Groups still exists as described | Not independently searched this session | Not verified this session; treated as negligible risk given ubiquity/longevity of the feature |

## Bottom line for the spine author

The spine's own convention of tagging unresolved external facts as `[ASSUMPTION]` is good practice and was applied correctly to the bio-link tool and (partially) to Google Flow. It should be extended to the two follower thresholds in AD-4, which currently read as confirmed facts but were not confirmed by anyone I can trace — including this review, which hit a tooling wall trying to check them. Before the operator treats "Shopee ≥500 / TikTok Shop ≥1.000" as a real go/no-go gate, those two numbers should be checked directly on Shopee's and TikTok Shop's own current affiliate-onboarding pages (ideally close to when each threshold is about to be hit, since these terms move).
