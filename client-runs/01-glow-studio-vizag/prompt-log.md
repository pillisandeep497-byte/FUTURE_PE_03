# Prompt Log — which prompt produced what

| # | Prompt | Output | Model | Notes |
|---|---|---|---|---|
| 1 | `prompts/00-seo-discovery-brief.md` | `discovery-brief.md` | Claude | 16-question intake + the free keyword research method (autosuggest, PAA, Trends, AnswerThePublic, Reddit, GBP insights, competitor indexes). |
| 2 | `prompts/01-keyword-cluster-architect.md` | `keyword-map.md`, `cluster-plan.md` | Claude; cross-checked on ChatGPT | 25 keywords classified by intent and funnel; cluster topology; cannibalisation check; internal-link matrix. 5 candidate topics were rejected with reasons (logged in `cluster-plan.md §2`). |
| 3 | `prompts/02-pillar-blog-outline.md` | Pillar outline (in `cluster-plan.md §3`) | Claude | H1–H3 only, word budget per section, PAA coverage map, E-E-A-T plan, schema plan. First draft had "Introduction"/"Conclusion" headings — removed. |
| 4 | `prompts/03-pillar-blog-writer.md` | `pillar-keratin-treatment-visakhapatnam.md` | Claude | ~1,968 words. First draft over-used the primary keyword (14 uses) — cut to 7. Answer-first rewrite applied to the opening. |
| 5 | `prompts/05-local-seo-adapter.md` | Local sections across the cluster + schema | Gemini | Local conditions (humidity, hard water, beach), landmarks, area price norms, GBP alignment, LocalBusiness JSON-LD. |
| 6 | `prompts/04-supporting-blog-generator.md` | The 5 support articles | Claude (4 runs) + ChatGPT (1) | One run per type — comparison, aftercare, objection, cost, local. Never batched, so no two articles share a structure. |
| 7 | `prompts/06-seo-qa-editorial-scorecard.md` | `qa-scorecard.md` | ChatGPT + manual | 12 audit findings (8 High), all fixed. Cluster average 42.8/44. 2026 policy gate applied. |
| 8 | — | `meta-titles-schema.md`, `internal-link-map.md` | Manual | Character counts verified with a counter. 15 internal links mapped with anchors. |
| 9 | — | `content-pack.md` | Manual assembly | Client-facing deck; internal notes removed. |

---

## Free-tool research actually performed (no paid SEO tool used)

| Method | What it produced | Used for |
|---|---|---|
| Google autosuggest | ~40 phrase variants across 12 prefixes | Keyword phrasing (customers say "straightening", not "smoothening") |
| People Also Ask + nested PAA | ~25 real questions | FAQ blocks in all six articles; H2 headings in the pillar |
| Related searches | ~15 adjacent queries | Support-article topics (comparison, aftercare, damage) |
| Google Trends (5-year + 12-month) | Seasonality read | Publishing schedule timed ahead of Nov–Feb wedding season |
| AnswerThePublic | Question groupings | Long-tail headings in S2 and S3 |
| Reddit / forum reading | Real complaints and failure stories | S3's failure-modes section, S4's "what the cheap option cuts" table |
| Competitor blog indexes (3 competitors) | ~35 titles | Gap analysis — none publish prices, process detail, or honest limitations |
| GBP query-insight method | — | Documented for the client; requires profile access |

**Note on demand figures:** no paid tool was available, so all volume figures in `keyword-map.md` are directional estimates marked `[E]`, each with a stated verification method (Keyword Planner, Trends, GBP Insights). Inventing precise volumes would have been the easy option and the wrong one.

---

## Model comparison (from actually running the work)

| Aspect | Claude | ChatGPT | Gemini |
|---|---|---|---|
| Long-form structure and flow | **Best** — holds a 2,000-word outline without drifting | Good | Prone to shorter, listier sections |
| Answer-first opening discipline | **Best** | Good, needs a reminder | Weakest — tends to write intros |
| Keyword balance without stuffing | **Best** | Good | Over-uses the primary keyword |
| Banned-phrase compliance | **Best** — self-corrects mid-generation | Good | Reintroduces clichés |
| Meta titles/descriptions within limits | Good (always recount) | Good | **Best** |
| Local SEO and schema | Good | Good | **Best** — cleanest JSON-LD |
| The QA/audit critique | Good | **Best** — genuinely blunt about weak sections | Moderate |
| Best role here | Pillar + supports + outlines | The audit and the objection article | Local adaptation + schema + metadata |

**Workflow used:** Claude for the pillar and most supports → Claude for the cluster architecture → Gemini for the local adaptation and JSON-LD → ChatGPT for the final audit. The same discovery brief was pasted into all three so no model worked from different facts.

---

## What I changed by hand

1. Cut the pillar from ~2,900 to ~1,968 words — every removal was explanation nobody asked for.
2. Rewrote the opening to lead with the price range instead of background.
3. Reduced the primary keyword from 14 uses to 7.
4. Added the studio's real 7-step process with timings, including why sealing takes 40–60 minutes.
5. Added the coastal-humidity, hard-water and beach sections — the content that makes the pillar genuinely local.
6. Built the "what the cheap option cuts" table in S4 from real failure modes found in forum research.
7. Removed all ten "Introduction/Conclusion/Overview" headings from the first drafts.
8. Hedged six outcome claims ("will last" → "usually lasts"; "repairs hair" → "leaves hair smoother").
9. Replaced generic "best salon in Visakhapatnam" targeting with the winnable MVP Colony local angle.
10. Added `[NEEDS CLIENT INPUT]` flags in place of ten numbers I could not verify.
