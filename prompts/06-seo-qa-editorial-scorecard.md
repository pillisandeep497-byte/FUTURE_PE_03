# PROMPT 06 — SEO QA & Editorial Scorecard

The gate. Run this on every article before it publishes — it catches the things that quietly kill rankings: intent mismatch, thin sections, cannibalisation, missing E-E-A-T, and the pattern Google now classifies as scaled content abuse.

---

## PART A — The editorial audit prompt

```
You are a senior SEO editor. Audit the article below against its target keyword and
intent. Be blunt — a false pass costs the client traffic.

ARTICLE: <paste full article>
TARGET PRIMARY KEYWORD: {{PRIMARY}}
TARGET INTENT: {{INTENT}}
PILLAR / SUPPORT ROLE: {{ROLE}}
SIBLING ARTICLES: <list their primary keywords>

AUDIT THESE 12 AREAS AND REPORT FINDINGS AS A TABLE
| # | Area | Finding | Severity | Fix |

1. INTENT MATCH — does the page deliver what the SERP rewards for this query?
   (If the SERP shows comparison pages and this is a definition, it will not rank.)
2. ANSWER-FIRST — is the query answered in the first 90 words?
3. HEADING DISCIPLINE — one H1; no skipped levels; no generic headings
   ("Introduction", "Conclusion"); every heading specific to this business.
4. KEYWORD BALANCE — primary in H1, first 100 words, one H2, meta.
   Report the exact count. Flag stuffing (>1% density) and flag absence.
5. CANNIBALISATION — does this page overlap a sibling's primary keyword or intent?
6. E-E-A-T — count the first-hand signals: real numbers, real process, named expert,
   local specifics, original photos briefed. Flag if fewer than 4.
7. INFORMATION GAIN — what does this page say that the current top-ranking pages
   don't? If the answer is "nothing", say so plainly.
8. CLAIM SAFETY — list every claim, statistic, price and result. Flag any without a
   source, a hedge, or a [NEEDS CLIENT INPUT] tag. Flag unverifiable superlatives.
9. READABILITY — paragraph length, sentence length, reading level, use of lists and
   tables, mobile scan-ability. Flag any paragraph over 4 sentences.
10. INTERNAL LINKING — are the required links present (supports: 2 up to pillar +
    1 sibling; pillar: down to every support)? Are the anchors descriptive?
11. SCHEMA & TECHNICAL — is the schema present and valid for the page type? Are the
    meta title (≤60) and description (≤155) within limits? Slug clean?
12. HELPFULNESS / SPAM RISK — would this page be classified as scaled or thin content?
    Specifically: is there any reason for this page to exist other than a keyword?
    Does it duplicate content available elsewhere without adding value?

THEN OUTPUT:
- A revised version of the article with every High-severity issue fixed
- A "STILL TO CONFIRM WITH CLIENT" list of every [NEEDS CLIENT INPUT] flag
```

---

## PART B — 30-point SEO scorecard

Score each published article. **Below 24 = do not publish.**

| # | Check | Weight | Score 0–2 |
|---|---|---|---|
| 1 | Primary keyword in H1, first 100 words, one H2, meta | x2 | |
| 2 | Query answered in the first 90 words | x2 | |
| 3 | Heading hierarchy clean (single H1, no skipped levels) | x1 | |
| 4 | Zero generic headings | x1 | |
| 5 | Intent matches what the SERP rewards for this query | x2 | |
| 6 | No overlap with a sibling's primary keyword or intent | x2 | |
| 7 | ≥4 first-hand E-E-A-T signals present | x2 | |
| 8 | Named author with a topic-relevant credential | x1 | |
| 9 | ≥1 piece of information gain vs current top results | x2 | |
| 10 | Real numbers where numbers are expected (price, time, count) | x2 | |
| 11 | Honest limitation / "who this is not for" section present | x2 | |
| 12 | Every claim sourced, hedged, or flagged | x2 | |
| 13 | No unverifiable superlatives | x2 | |
| 14 | Paragraphs ≤4 sentences; sentences avg ≤18 words | x1 | |
| 15 | At least one table and one list | x1 | |
| 16 | FAQ block of 4+ questions matching People Also Ask | x1 | |
| 17 | Internal links correct in count and anchor quality | x2 | |
| 18 | Meta title ≤60 chars, description ≤155 chars, counts verified | x1 | |
| 19 | Schema present and valid for the page type | x1 | |
| 20 | Local mentions natural (2–4), all true, no stuffing | x2 | |
| 21 | Photo brief with descriptive alt text supplied | x1 | |
| 22 | No banned phrases present | x1 | |
| 23 | CTA is specific, low-friction, and states what happens next | x1 | |
| 24 | Passes the city-name-swap test (if local-targeted) | x2 | |
| 25 | Would pass Google's scaled-content-abuse test (page has a reason to exist) | x2 | |
| 26 | Comparison to top 3 competitors: does this add anything they lack? | x1 | |
| 27 | Title is clickable without being clickbait | x1 | |
| 28 | Content is dated and has an update plan | x1 | |
| 29 | Readable by the target customer (no unexplained jargon) | x1 | |
| 30 | You would publish this under your own name | x2 | |

**Max 44.** 38+ publish · 30–37 fix and publish · 24–29 rewrite the weak sections · below 24 don't publish.

---

## PART C — The 2026 policy gate (read before publishing anything)

Google does **not** ban AI-assisted content. It targets content that exists to manipulate rankings rather than help people, under the **scaled content abuse** policy — and the March 2026 core update made that its primary enforcement target, with reported 50–80% traffic drops for sites hit.

| Risk pattern | What it looks like | How this system avoids it |
|---|---|---|
| **Scaled content abuse** | Hundreds of pages, template with variables swapped | Cluster of 6 deeply-researched articles, published at a rate the business can review |
| **Thin location pages** | "[Service] in [City]" repeated for 40 localities, nothing local inside | One genuinely local article, passing the city-swap test |
| **No authorship** | Anonymous posts, no credentials, no accountability | Named author with a relevant credential on every article |
| **No information gain** | Rewriting what's already on page one | Required "information gain" section in the audit; real prices, processes, refusals |
| **Keyword-driven existence** | The page exists because a keyword exists | Every article must answer a question a real customer asked |
| **Undeclared freshness manipulation** | Changing dates without changing content | "Last updated" only when content actually changes |

**Publish-rate rule (the one most people get wrong):** never publish faster than you can personally review, fact-check and add first-hand detail to. A 6-article cluster published over 3 months with care will outrank a 60-article site published in a week — and it won't carry the collapse risk.

---

## PART D — Pre-publish technical checklist

- [ ] URL slug: short, keywords, hyphens, no dates
- [ ] Title tag ≤60 characters (verify with a counter, not by eye)
- [ ] Meta description ≤155 characters, benefit + proof + action
- [ ] H1 matches the title intent (need not be identical)
- [ ] One H1 on the page only
- [ ] Images compressed (WebP where possible), descriptive file names, alt text written
- [ ] Internal links: correct count, descriptive anchors, no broken targets
- [ ] External sources linked where claims are made
- [ ] Schema JSON-LD validated (Rich Results Test)
- [ ] Canonical tag self-referencing
- [ ] Added to the sitemap; sitemap resubmitted in Search Console
- [ ] Mobile check: tables scroll, text readable without zoom, tap targets fine
- [ ] Page speed: images lazy-loaded, no render-blocking scripts added
- [ ] Author bio block present and linked to an author page
- [ ] Published date + last-updated date visible
- [ ] CTA present and functional (WhatsApp link tested on a phone)
- [ ] Indexed check scheduled for 7 days post-publish (site: query / URL inspection)
- [ ] Search Console tracking: add the URL to a monthly performance note

---

## PART E — The 90-day measurement plan (what to tell the client)

| Timeframe | What to check | What "working" looks like |
|---|---|---|
| Week 1–2 | Indexation | Every published URL is indexed |
| Week 3–6 | Impressions in Search Console | Impressions rising even at position 40+ — that means relevance is recognised |
| Month 2 | Position movement | Target keywords moving from page 3–4 to page 2 |
| Month 3 | Clicks and conversions | First clicks on commercial-intent pages; first enquiry you can attribute to a blog |
| Month 6 | Compounding | The pillar ranking for its primary keyword; supports ranking for long-tails; internal links pushing the pillar up |

**Set expectations correctly, in the client's words:** "You will not see leads in week two. Impressions come first, then positions, then clicks. Month three is when you can judge it."
