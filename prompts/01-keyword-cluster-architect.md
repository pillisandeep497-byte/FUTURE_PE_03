# PROMPT 01 — Keyword Cluster Architect

**This is the prompt that separates an SEO system from "posting articles".** It turns raw seed keywords into a topology: one pillar, 4–6 supports, each with a distinct primary keyword, a distinct intent, and an internal-linking role.

---

## The prompt

```
# ROLE
You are a technical SEO strategist who designs content clusters. You know that a
cluster fails when two pages target the same query (cannibalisation), when a support
article has no reason to link to the pillar, or when the pillar targets an
informational query that can never convert.

# INPUTS
SEO DISCOVERY BRIEF: <paste brief>
RAW KEYWORD LIST: <paste seeds from autosuggest, PAA, related searches, GBP insights>
COMPETITOR TITLES: <paste competitor blog titles if available>
PUBLISHING CAPACITY: {{CAPACITY}} articles/month

# TASK

1. KEYWORD TABLE — every seed keyword, classified:
   | Keyword | Intent | Funnel stage | Est. monthly demand | Competition read | Business value | Cluster |
   - Intent: informational | commercial-investigation | transactional | navigational | local
   - Funnel: TOFU / MOFU / BOFU
   - Est. monthly demand: LOW (<100) / MED / HIGH (1,000+) — mark every value [ESTIMATE]
     and state how to verify it (Google Keyword Planner, GBP insights, Trends)
   - Competition read: what kind of pages currently rank (directory/local pack,
     big brand blog, small local site, forum)? This is more actionable than any
     difficulty score.
   - Business value: H/M/L — does ranking here lead to a paid job?

2. CLUSTER TOPOLOGY — design the structure:
   - ONE pillar article: the broadest commercially-relevant topic you can own.
     Its primary keyword must be one a buyer could plausibly search.
   - 4–6 supporting articles. For each, specify its type:
       · COMPARISON   — "X vs Y vs Z"
       · OBJECTION    — "will X damage/break/is X worth it"
       · HOW-TO       — "how to make X last / prepare for X"
       · COST         — "X price/cost breakdown"
       · LOCAL        — "[service] in [area]" / "how to choose a [category] in [city]"
       · FAQ/HUB      — a roundup of the questions from the brief
   - Explain in one line why each support article exists and how it links up to the pillar.

3. CANNIBALISATION CHECK — produce a table proving no two articles share a primary
   keyword, and that no two would satisfy the same query. If two are too close,
   merge them and say so.

4. INTERNAL LINK MATRIX — a grid: rows = articles, columns = articles.
   Mark P (links to pillar with exact/partial anchor), S (links to a sibling),
   — (no link needed). Every support must link UP to the pillar at least twice:
   once in the first 150 words, once near the end. The pillar must link DOWN to
   every support. Specify the anchor text for each link — it must be descriptive,
   not "click here".

5. PRIORITY ORDER — rank the articles by (business value × intent) ÷ effort.
   State which single article to publish FIRST and why.

6. KEYWORD MAPPING TABLE (the deliverable a developer works from):
   | URL slug | Primary keyword | Secondary keywords (3–5) | Title tag (≤60) | Meta description (≤155) | H1 | Target SERP features |

# HARD CONSTRAINTS
- One primary keyword per page. Zero exceptions. A page targeting two primaries
  ranks for neither.
- Every keyword must connect to a service the business actually sells.
- The pillar must target commercial or commercial-investigation intent — never pure
  TOFU curiosity, unless the business goal is awareness.
- Local keywords must use the real area/city from the brief, and only areas the
  business actually serves.
- If {{CAPACITY}} is under 4 per month, cut the cluster to 1 pillar + 3 supports and
  say so. Do NOT design a 12-article cluster for a business that can publish 2 a
  month — publishing beyond review capacity is the fastest route to a
  scaled-content problem.
- No article may be a templated "[service] in [city]" page unless the article
  contains genuinely local detail (landmarks, local conditions, real local photos,
  area-specific advice). Template-and-swap location pages are explicitly penalised.

# BANNED
Keyword-stuffed titles · "best [service] in [city]" unless the page genuinely
compares and evidences it · "[city] [service] [city] [service]" repetition ·
doorway-page patterns · two pages targeting singular/plural variants of the same
phrase · article titles that promise data the business doesn't have.

# OUTPUT FORMAT
Markdown: sections 1–6 in order. Then a one-paragraph STRATEGY SUMMARY a business
owner could read and understand, in plain language, with no jargon.

# SELF-CHECK
1. Could a stranger tell which page targets which query, without asking?
2. Does every support have a genuine reason to exist beyond keyword volume?
3. Is the cluster small enough to be published with editorial care at {{CAPACITY}}?
4. Would each article contain at least one thing competitors can't reproduce?
5. Any two pages competing for the same query? 
End with "--- CLUSTER ARCHITECTURE READY ---" and scores (Intent clarity,
Cannibalisation safety, Internal-link logic, Business alignment, Scalability safety)
each 1–5.
```

---

## The cluster pattern that works for local businesses

```
                    ┌─────────────────────────────┐
                    │        PILLAR ARTICLE       │
                    │  "Keratin Treatment in      │
                    │   Visakhapatnam: Cost,      │
                    │   Process & Results"        │
                    │  (commercial-investigation) │
                    └──────────────┬──────────────┘
        ┌──────────────┬───────────┼───────────┬──────────────┐
        ▼              ▼           ▼           ▼              ▼
   COMPARISON     OBJECTION     HOW-TO       COST          LOCAL
   keratin vs     will it       make it      price         salon in
   smoothening    damage hair   last longer  breakdown     MVP Colony
   vs botox
   (MOFU)         (MOFU)        (TOFU/MOFU)  (BOFU)        (BOFU/local)
```

**Why this shape:**
- The **pillar** owns the buying-intent query and converts.
- **Comparison** and **objection** articles catch people mid-decision and hand them to the pillar.
- **How-to** earns the informational traffic that builds topical authority — and links up.
- **Cost** is the highest-intent support and often converts better than the pillar.
- **Local** captures "near me" demand that the pillar can't, because the pillar is topic-led, not place-led.

**Rule:** every support article links to the pillar twice and to one sibling once. The pillar links to every support. No orphans.

---

## Cannibalisation: the check most people skip

| Symptom | What happened | Fix |
|---|---|---|
| Two pages alternate positions for one query in Search Console | Two pages target the same intent | Merge them, 301 the weaker one |
| A support outranks the pillar for the pillar's keyword | Support is more specific than the pillar | Rewrite the support to target a narrower long-tail, and link up harder |
| A page ranks for nothing after 3 months | Intent mismatch, or the keyword has no real demand | Re-check demand; rewrite the H1 to match the actual SERP intent |
| Rankings drop after adding a new article | The new article overlaps an existing one | Run the matrix before publishing, not after |
