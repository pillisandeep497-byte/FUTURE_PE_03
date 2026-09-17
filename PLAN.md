# Execution Plan — Future Interns, Prompt Engineering Task 3 (2026)
## "AI SEO Blog & Content Cluster Generator for Business Websites"

**Intern:** Pilli Sandeep
**Chosen business:** Glow Studio by Sanjana — hair & bridal studio, MVP Colony, Visakhapatnam
**Cluster:** Keratin treatment (1 pillar + 5 supporting articles)
**Total time budget:** ~10 hours across 6 sessions

---

## 0. What's actually being graded

| Task requirement | Where it lives | Proof |
|---|---|---|
| Generate **SEO blog outlines (H1–H3)** | `prompts/02-pillar-blog-outline.md` + every article's heading structure | Outlines with word budgets, section "jobs", PAA coverage map |
| **Write long-form, helpful blog content** | `client-runs/.../pillar-*.md` + 5 support articles | 8,550 words of publish-ready content |
| **Create content clusters** (pillar + supporting) | `cluster-plan.md` | Cluster map, 1 pillar + 5 supports, internal-link matrix, cannibalisation check |
| **Adapt for local SEO** (city + service) | `prompts/05-local-seo-adapter.md`, `support-05-hair-salon-mvp-colony*.md` | Genuine local content: humidity, landmarks, local pricing, seasonality |
| Support business goals (leads, trust, authority) | `content-pack.md` §Measurement + CTA blocks | Intent-to-funnel mapping; every article ends in a low-friction action |
| SEO structure: headings, internal linking, readable sections, business conclusions | `internal-link-map.md`, `meta-titles-schema.md`, each article | Link matrix with anchors; 30-point scorecard per article |
| ✔ SEO-optimized outlines | ✓ | 6 articles, H1–H3 only, word budgets |
| ✔ Clear search intent targeting | `keyword-map.md` | Every keyword classified by intent + funnel stage |
| ✔ Content clusters | ✓ | Pillar + 5 supplies, 15 internal links, 0 cannibalisation |
| ✔ Local SEO focus | ✓ | Area/city keywords, landmarks, GBP alignment, local schema |
| ✔ Helpful, human-readable content | `qa-scorecard.md` | Readability scores, banned-phrase scan, information-gain requirement |
| ✔ Reusable prompt structure | `prompts/00`–`06` | Variable-driven; 6 industries proven in `adaptability-proof.md` |
| **Complete SEO Content Pack** | `content-pack.md` | Strategy + keyword/intent explanation + all 6 articles |
| Public GitHub repo | this folder | ⬜ push |
| LinkedIn showcase | `docs/linkedin-post.md` | 3 ready-to-post writeups | ⬜ post |

**The differentiator:** most submissions dump "SEO prompts". This one is built around a **2026-specific constraint** — Google's *scaled content abuse* enforcement (the March 2026 core update made it the primary target, with 50–80% traffic drops for hit sites). So the system deliberately produces **fewer, deeper, first-hand articles** with a publish-rate rule tied to review capacity, plus an information-gain requirement in the audit. That is what a real SEO lead would build today, and it shows you know what changed.

---

## 1. The six sessions

### Session 1 — Discovery + free keyword research (2 hr)
1. Run `prompts/00` with the owner, or fill it from their site, GBP and reviews if you can't get a meeting.
2. Do the free research in `prompts/00` Part C: Google autosuggest (12 prefixes), People Also Ask chains, related searches, Trends (5-year + 12-month view), AnswerThePublic, Reddit/Quora, GBP query insights, competitor blog indexes.
3. Output: 80–120 raw keywords. **Do not skip this session.** Everything downstream inherits its quality.

### Session 2 — Cluster architecture (1.5 hr)
1. Run `prompts/01` → keyword table with intent + funnel + business value, cluster topology, cannibalisation check, internal-link matrix.
2. Decide scope against publishing capacity. For a small local business: **1 pillar + 5 supports over 3 months**, not 12 articles in 3 weeks.
3. Write `keyword-map.md` and `cluster-plan.md`.

### Session 3 — Pillar article (2.5 hr)
1. `prompts/02` → outline with word budgets, PAA map, E-E-A-T plan, schema plan.
2. `prompts/03` → the full article (~2,000 words).
3. `prompts/05` → local adaptation (humidity, landmarks, local pricing, seasonality).
4. Human pass: add the local/experience details a model can't know; cut every generic paragraph.

### Session 4 — Supporting articles (2.5 hr)
1. `prompts/04`, one run per type: comparison, objection, how-to/aftercare, cost, local.
2. Stagger angles so no two articles share a structure.
3. Keep each 700–1,300 words — complete beats padded.

### Session 5 — Structure, metadata, links (1 hr)
1. `internal-link-map.md` — full matrix with anchor text.
2. `meta-titles-schema.md` — title tags, meta descriptions (counts verified), slugs, JSON-LD for Article + FAQPage + LocalBusiness/Service.
3. Image briefs with alt text per article.

### Session 6 — QA, packaging, shipping (1.5 hr)
1. `prompts/06` on every article → fix all High-severity findings. Record the scores.
2. Assemble `content-pack.md` (client deliverable).
3. Open `preview/index.html` in a browser and screenshot it for LinkedIn (`preview/README.md` lists the three crops worth taking).
4. Push to GitHub (`ai-seo-content-cluster`), post on LinkedIn tagging Future Interns, then pitch the business.

---

## 2. Deliverables checklist

```
✅ SEO Content Pack        → client-runs/01-glow-studio-vizag/content-pack.md
   ├── 1 pillar blog       → pillar-keratin-treatment-visakhapatnam.md   (1,968 words)
   ├── 5 supporting blogs  → support-01 … support-05                     (~6,585 words)
   ├── keyword + intent    → keyword-map.md
   └── cluster + links     → cluster-plan.md, internal-link-map.md
✅ Structured prompts      → prompts/00 … 06
✅ Documentation           → README.md, PLAN.md, prompt-log.md, qa-scorecard.md
✅ LinkedIn showcase       → docs/linkedin-post.md
✅ Reusability proof       → client-runs/adaptability-proof.md (6 industries)
✅ Visual preview          → preview/index.html + preview/images/ (6 visuals)
✅ Documentation set       → docs/submission-checklist.md · linkedin-post.md ·
                             client-outreach-and-seo-packages.md · tools-and-workflow.md
⏳ Public GitHub repo      → push with PUBLISH.md (folder structure safe)
⏳ LinkedIn showcase       → docs/linkedin-post.md (tag Future Interns)
⏳ Client delivery         → send content-pack.md, then pitch docs/client-outreach-and-seo-packages.md
```

---

## 3. Exact GitHub commands

```bash
cd ~/ai-seo-content-cluster
git init
git add .
git commit -m "feat: AI SEO content cluster system + 6-article pack (Glow Studio, Vizag)"
git branch -M main
git remote add origin https://github.com/pillisandeep497-byte/ai-seo-content-cluster.git
git push -u origin main
```

**Repo description:** `Reusable prompt system that generates SEO content clusters for business websites — keyword mapping, pillar + supporting blogs, internal linking, local SEO and a scaled-content-safe QA gate. Future Interns Prompt Engineering Task 3.`
**Topics:** `seo`, `content-clusters`, `prompt-engineering`, `local-seo`, `content-marketing`, `future-interns`

⚠️ **Upload with the create-folder-first method** in `PUBLISH.md` — drag-and-drop flattens folder structure, which is what happened to Task 1.

---

## 4. Selling this (the Learn & Earn part)

| Package | Deliverable | Suggested price |
|---|---|---|
| **SEO audit + keyword map** | Discovery brief, 25-keyword map with intent, cluster plan (+ competitor gap analysis) | ₹3,000 one-time |
| **Starter cluster** | 1 pillar + 3 supports, internal links, meta, schema | ₹8,000 |
| **Standard cluster** ⭐ | 1 pillar + 5 supports + local SEO setup (GBP + schema) | ₹15,000 |
| **Monthly SEO content** | 2 articles/month + internal linking + Search Console reporting | ₹8,000/month |
| **Retainer + technical** | Content + on-page fixes + GBP management + monthly report + link opportunities | ₹15,000–₹25,000/month |

**Market context:** SEO agencies in India charge ₹15,000–₹40,000/month retainers for exactly this work. A local business owner will pay ₹8,000–₹15,000 for a well-researched cluster once they understand it compounds.

**Your pitch line:** *"Six articles that work together will beat sixty that don't. Here's the map — one pillar, five supports, all internally linked, all answering a question your customers actually typed."*

Full pitch scripts: `docs/client-outreach-and-seo-packages.md`.

---

## 5. Do-not-skip

1. **Do the real keyword research.** Autosuggest and People Also Ask take 45 minutes and are the difference between a real cluster and an invented one. Never let the model invent search demand.
2. **One primary keyword per page.** Two pages for one query means neither ranks.
3. **Keep the information-gain section.** If an article says nothing the top results don't already say, don't publish it.
4. **Publish at your review capacity.** Six careful articles in three months beats sixty in a week — and avoids the scaled-content risk entirely.
5. **Real prices in the cost article.** It's the highest-intent page in the cluster and the one most competitors leave blank.
6. **Flag every unverified number** with `[NEEDS CLIENT INPUT]`. Never invent a statistic, a review count or a credential — in a YMYL-adjacent category like beauty/health, that's a trust and legal problem.
