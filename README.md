# AI SEO Content Cluster System

**A reusable prompt workflow that plans and writes SEO content clusters for business websites — keyword mapping, one pillar article, supporting articles, internal linking, local SEO and a scaled-content-safe QA gate.**

Built for **Future Interns — Prompt Engineering Task 3 (2026)**.

**Author:** Pilli Sandeep · **Contact:** WhatsApp +91 91002 12761
**Repository:** [github.com/pillisandeep497-byte/ai-seo-content-cluster](https://github.com/pillisandeep497-byte/ai-seo-content-cluster)

---
**live link:** https://deft-sherbet-e51d3a.netlify.app/
## What problem this solves

Most business websites don't get traffic because they "post articles" instead of building strategy. Content goes up randomly, nothing internally links, keywords overlap, and the pages that could convert have no prices in them.

This system does what an SEO agency does: it starts with a **discovery brief**, does **free keyword research**, designs a **cluster topology** (one pillar + supporting articles with one keyword each), writes **answer-first long-form content**, wires the **internal links**, adapts for **local search**, and then **audits every article against a 30-point scorecard** before publishing.

**The 2026-specific constraint that shapes this whole system:** Google does not ban AI-assisted content — its spam policy targets **scaled content abuse** (many low-value pages created mainly to manipulate rankings), and the March 2026 core update made that its primary enforcement target, with reported 50–80% traffic drops for sites hit. So this system deliberately produces **fewer, deeper, first-hand articles**, with a publish-rate rule tied to how much content the business can actually review. That's the difference between a system that ranks and one that eventually collapses.

**Sources:** [Google's AI content policy and scaled content abuse](https://rankai.ai/articles/google-policy-on-ai-content-seo-compliance-guide) · [March 2026 enforcement analysis](https://www.digitalapplied.com/blog/scaled-content-abuse-google-march-update-ai-pages-decimated)

---

## The client run

**Glow Studio by Sanjana** — hair & bridal studio, 1st Floor, above Sri Sai Bakery, MVP Colony Main Road, Sector 4, Visakhapatnam
7 years operating · keratin, smoothening, colour and bridal services · 4 chairs

**The cluster:** keratin treatment — 1 pillar + 5 supporting articles (8,550 words), built around the single biggest content gap found in competitor research: **nobody in the city publishes prices, process detail or honest limitations.**

> ⚠️ **Integrity note:** Glow Studio is a **representative demonstration business**, not a verified paying client. Every price, count and credential is marked `*(verify)*` or `[NEEDS CLIENT INPUT]`. All keyword demand figures are directional estimates marked `[E]` — no paid SEO tool was used, and the verification method is stated for each. Replace these with real numbers before publishing anything.

📄 Brief: [`client-runs/01-glow-studio-vizag/discovery-brief.md`](client-runs/01-glow-studio-vizag/discovery-brief.md)

---

## What the system produces

| Output | What's inside |
|---|---|
| **Keyword & intent map** | 25 keywords classified by intent + funnel stage + business value, with a competition read stating *what kind of pages currently rank* — more actionable than a difficulty score |
| **Cluster topology** | 1 pillar + 5 supports; each support has a type, a job, and a reason to exist beyond keyword volume |
| **Cannibalisation check** | A table proving no two pages compete for the same query, plus the one risk found and how it's handled |
| **Pillar article** | 1,968 words, answer-first, 7-step process with real timings, cost table, "who this is NOT for", local conditions, 8 FAQs |
| **5 supporting articles** | Comparison · aftercare/how-to · objection · cost · local — each 1,235–1,397 words, one primary keyword each |
| **Internal link matrix** | 15 links with anchor text and exact placement, plus the site-wide links that must exist |
| **Local SEO layer** | Real local content (coastal humidity, hard water, landmarks, area price norms), GBP alignment checklist, LocalBusiness + Service + FAQPage schema |
| **Meta + schema** | Title tags and descriptions counted to character, slugs, and copy-paste JSON-LD |
| **QA gate** | 30-point scorecard per article + the 2026 policy gate + a pre-publish technical checklist |

---

## The prompt logic (how the system works)

Every prompt uses the same eight-part skeleton:

```
ROLE → BRIEF (source of truth) → TASK → HARD CONSTRAINTS → BANNED LIST
→ OUTPUT FORMAT → QUALITY BAR → SELF-CHECK
```

**Seven decisions that make the output rank instead of just read well:**

| Decision | Why it matters |
|---|---|
| **Discovery before keywords** | The brief captures services, geography, proof and *pre-purchase questions*. Keywords without business context produce traffic that never converts. |
| **Free research, stated method** | Autosuggest, People Also Ask (including nested PAA), related searches, Trends, AnswerThePublic, forums, competitor indexes. Every estimate carries its verification method rather than a fake precision. |
| **One primary keyword per page, enforced** | Two pages for one query means neither ranks. The cannibalisation check is a required output, not an afterthought. |
| **Answer-first in the first 90 words** | Wins featured snippets and AI Overview citations, and respects a reader who is about to spend money. |
| **"Who this is NOT for" is mandatory** | The strongest E-E-A-T signal available to a local business, and the one thing no competitor writes. |
| **Information gain is a scored criterion** | If an article says nothing the current top results don't already say, it doesn't get published. This is also the direct answer to Google's scaled-content policy. |
| **Publish-rate rule tied to review capacity** | The system reads publishing capacity from the brief and sizes the cluster to it, and refuses to design 12-article clusters for businesses that can review 2 a month. |

**Reusability:** only the discovery brief changes between clients. See [`client-runs/adaptability-proof.md`](client-runs/adaptability-proof.md) — same system applied to a dental clinic (YMYL), coaching institute (dual audience), digital agency (B2B), SaaS tool (compliance-driven) and diagnostic centre (hyper-local + branch pages), each with a different cluster shape.

---

## Tools used

| Tool | Role |
|---|---|
| **Claude** | Cluster architecture, pillar article, supporting articles — best at holding long outlines and answer-first discipline |
| **ChatGPT** | The editorial audit and objection-article drafting — genuinely blunt about weak sections |
| **Gemini** | Local SEO adaptation, metadata, JSON-LD schema |
| **Google Search (autosuggest, PAA, related searches)** | Real query phrasing and the FAQ spine of the cluster |
| **Google Trends** | Seasonality and trend direction before committing to a cluster |
| **AnswerThePublic · Reddit/forums · competitor blog indexes** | Long-tail questions and the gaps nobody has filled |

**No paid SEO tool was used.** Full workflow: [`docs/tools-and-workflow.md`](docs/tools-and-workflow.md)

---

## Repository structure

```
.
├── prompts/                                     ← THE SYSTEM
│   ├── 00-seo-discovery-brief.md                ← 16-question brief + the free keyword research method
│   ├── 01-keyword-cluster-architect.md          ← intent mapping, cluster topology, cannibalisation check
│   ├── 02-pillar-blog-outline.md                ← H1–H3 outlines, PAA coverage, schema plan
│   ├── 03-pillar-blog-writer.md                 ← long-form writer with E-E-A-T and answer-first rules
│   ├── 04-supporting-blog-generator.md          ← 6 support types with distinct jobs
│   ├── 05-local-seo-adapter.md                  ← city+service, GBP, local schema, doorway-page guard
│   └── 06-seo-qa-editorial-scorecard.md         ← 12-area audit + 30-point scorecard + 2026 policy gate
│
├── client-runs/
│   ├── 01-glow-studio-vizag/
│   │   ├── discovery-brief.md
│   │   ├── keyword-map.md                       ← 25 keywords + intent + cluster topology + priority order
│   │   ├── cluster-plan.md                      ← article briefs, rejected topics, calendar, measurement
│   │   ├── pillar-keratin-treatment-visakhapatnam.md      ← ⭐ the pillar (1,968 words)
│   │   ├── support-01-keratin-vs-smoothening-vs-botox.md
│   │   ├── support-02-how-to-make-keratin-last.md
│   │   ├── support-03-does-keratin-damage-hair.md
│   │   ├── support-04-keratin-treatment-cost.md           ← publish this first
│   │   ├── support-05-hair-salon-mvp-colony.md
│   │   ├── internal-link-map.md                 ← 15 links with anchors and placement
│   │   ├── meta-titles-schema.md                ← titles, metas, slugs, JSON-LD
│   │   ├── qa-scorecard.md                      ← 30-point scores + policy gate + blockers
│   │   ├── prompt-log.md                        ← what produced what, model comparison
│   │   └── content-pack.md                      ← ⭐ the deliverable you hand the client
│   └── adaptability-proof.md                    ← 1 system, 6 industries, 6 cluster shapes
│
├── preview/
│   ├── index.html                               ← visual content pack (screenshot for LinkedIn)
│   ├── README.md                                ← what the page shows + which images to replace
│   └── images/                                  ← 6 concept visuals (AI-generated) + README
├── docs/
│   ├── submission-checklist.md                  ← every task requirement → the file that satisfies it
│   ├── linkedin-post.md                         ← ready-to-post writeups
│   ├── client-outreach-and-seo-packages.md      ← pitch scripts + pricing packages
│   └── tools-and-workflow.md                    ← the free-tool workflow, end to end
├── PLAN.md · PUBLISH.md · LICENSE · .gitignore
```

---

## How to reuse for another client

1. **Discovery** (`prompts/00`) — 16 questions with the owner, plus 45 minutes of free keyword research.
2. **Architecture** (`prompts/01`) — intent map, cluster topology, cannibalisation check, priority order.
3. **Outline and write the pillar** (`prompts/02`, `prompts/03`).
4. **Adapt for local** (`prompts/05`) — real local conditions, GBP alignment, schema.
5. **Write 4–6 supports** (`prompts/04`) — one run per type, never batched.
6. **Audit** (`prompts/06`) — fix every High finding, clear the policy gate, then publish at your review capacity.

**Time per client:** ~3 hours for the full pack once the system exists. That's what makes ₹8,000–₹15,000 per cluster viable.

---

## Results

| Metric | Result |
|---|---|
| Published-ready content | 6 articles · **8,550 words** |
| Keywords mapped | 25, classified by intent, funnel and business value |
| Cluster structure | 1 pillar + 5 supports · 15 internal links · 0 orphan pages |
| Cannibalisation risks | 1 identified and resolved (pillar vs cost article) |
| QA score | **42.8 / 44 cluster average** (all six above the publish threshold) |
| Editorial findings fixed | 12 (8 High severity) |
| Information-gain sections | 6 — one per article |
| Industries the system has been proven on | 6 |

---

## Honest limitations

- **Keyword volumes are estimates.** No paid tool was used; every figure is marked `[E]` with a stated verification method. Verify in Keyword Planner or GBP Insights before committing budget.
- **Rankings aren't guaranteed and can't be.** The system optimises structure, intent match and content quality. Google decides.
- **Schema and metadata are provided, not installed.** A developer still needs to paste the JSON-LD, set canonicals, add to the sitemap and compress images.
- **It needs real photos and real numbers.** Stock salon photos and invented client counts would undo the E-E-A-T work these articles are built on.
- **It needs an author.** Beauty and health-adjacent content requires a named, credentialed human. `[NEEDS CLIENT INPUT]` flags mark every place the client must supply facts — that flagging is deliberate, not incomplete work.

---

## License

MIT. Prompt system designed by **Pilli Sandeep** for the Future Interns Prompt Engineering Internship, 2026. The "Glow Studio by Sanjana" client profile is a representative demonstration, not a verified business record.
