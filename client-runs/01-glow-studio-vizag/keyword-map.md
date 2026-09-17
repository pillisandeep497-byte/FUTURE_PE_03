# Keyword Map & Search Intent Analysis
**Client:** Glow Studio by Sanjana · **Cluster:** Keratin treatment · **Prompt used:** `prompts/01-keyword-cluster-architect.md`

> **On the numbers:** no paid SEO tool was used for this project. Demand bands below are directional reads from Google autosuggest ordering, People Also Ask depth, Trends relative interest, and the number of weak pages ranking (a high number of thin results usually signals attainable demand). Every demand figure is marked `[E]` = estimate. **Verification method is stated for each so the client or agency can confirm it in Google Keyword Planner, Google Trends or GBP Insights before committing budget.**

---

## 1. Keyword table

| # | Keyword | Intent | Funnel | Est. demand `[E]` | What currently ranks | Business value | Cluster |
|---|---|---|---|---|---|---|---|
| 1 | keratin treatment in visakhapatnam | Commercial-investigation | MOFU | MED–HIGH | Local salon pages + directory listings, all thin, no prices | **H** | **PILLAR** |
| 2 | keratin treatment cost in visakhapatnam | Commercial-investigation | BOFU | MED | Almost nothing specific — a real gap | **H** | Support 04 (cost) |
| 3 | keratin treatment price visakhapatnam | Commercial | BOFU | MED | Same gap | **H** | Support 04 |
| 4 | how long does keratin last | Informational | TOFU/MOFU | HIGH | Big beauty sites, generic, no local angle | M | Support 02 |
| 5 | keratin aftercare / care after keratin | Informational | MOFU | MED | Generic blogs, no India/coastal context | M | Support 02 |
| 6 | does keratin damage hair | Informational (objection) | MOFU | HIGH | Big sites, mostly brand-safe answers, no honest local voice | **H** | Support 03 |
| 7 | is keratin treatment safe | Informational (objection) | MOFU | MED–HIGH | Health sites, patchy | H | Support 03 |
| 8 | keratin vs smoothening | Commercial-investigation | MOFU | HIGH | Big sites + forums; nothing local | **H** | Support 01 |
| 9 | keratin vs hair botox | Commercial-investigation | MOFU | MED | A few generic posts | H | Support 01 |
| 10 | hair smoothening vs straightening | Commercial-investigation | MOFU | MED | Generic | M | Support 01 |
| 11 | hair salon in mvp colony | Local | BOFU | MED | Local pack + directories | **H** | Support 05 |
| 12 | hair salon near mvp colony visakhapatnam | Local | BOFU | MED | Local pack | H | Support 05 |
| 13 | best salon in visakhapatnam | Local | BOFU | HIGH | Directories, aggregators — hard to win, not targetable | L | Skip |
| 14 | keratin treatment near me | Local | BOFU | HIGH | Local pack — GBP wins this, not articles | H | GBP (not an article) |
| 15 | hair botox treatment visakhapatnam | Commercial | MOFU | LOW–MED | Near-empty | M | Support 01 |
| 16 | how long does keratin treatment take | Informational | MOFU | MED | Generic | M | Pillar H2 |
| 17 | can i wash hair after keratin | Informational | MOFU | MED | Generic, inconsistent advice | M | Support 02 |
| 18 | keratin treatment for curly hair | Informational | MOFU | MED | Big sites | M | Support 01 |
| 19 | hair smoothening cost visakhapatnam | Commercial | BOFU | MED | Thin | H | Support 04 |
| 20 | bridal makeup artist visakhapatnam | Commercial | BOFU | HIGH | Many strong pages | H | **Phase-2 cluster** |
| 21 | pre bridal package visakhapatnam | Commercial | BOFU | MED | Few, weak | H | **Phase-2 cluster** |
| 22 | keratin treatment benefits and side effects | Informational | TOFU | MED | Health/beauty sites | M | Support 03 |
| 23 | frizzy hair treatment in visakhapatnam | Informational→commercial | MOFU | LOW–MED | Thin | M | Pillar (secondary) |
| 24 | keratin treatment near visakhapatnam humidity | Long-tail local | MOFU | LOW | Nothing | M | Pillar (local section) |
| 25 | best hair salon mvp colony review | Local | BOFU | LOW | Nothing | M | Support 05 |

**Legend:** `[E]` = estimated demand band, verify before committing. Demand bands: LOW <100/mo · MED 100–1,000 · HIGH 1,000+.

**Verification method for each:** Google Keyword Planner (free with a Google Ads account, even without spend) for volume · Google Trends for seasonality and trend direction · GBP Insights → Search queries for first-party demand · autosuggest ordering for relative demand within a topic.

---

## 2. Cluster topology

```
                        ┌──────────────────────────────────────────┐
                        │           PILLAR ARTICLE                 │
                        │  "Keratin Treatment in Visakhapatnam:    │
                        │   Cost, Process, Results & Honest Advice"│
                        │   Primary: keratin treatment in          │
                        │            visakhapatnam                 │
                        │   ~1,968 words · commercial-investigation│
                        └────────────────┬─────────────────────────┘
        ┌──────────────┬────────────────┼────────────────┬──────────────┐
        ▼              ▼                ▼                ▼              ▼
  ┌───────────┐ ┌─────────────┐ ┌─────────────┐ ┌────────────┐ ┌──────────────┐
  │ SUPPORT 1 │ │  SUPPORT 2  │ │  SUPPORT 3  │ │ SUPPORT 4  │ │  SUPPORT 5   │
  │ COMPARISON│ │   HOW-TO    │ │  OBJECTION  │ │    COST    │ │    LOCAL     │
  │ keratin vs│ │ how to make │ │ does keratin│ │ keratin    │ │ choosing a   │
  │ smoothening│ │ keratin last│ │ damage hair?│ │ cost in    │ │ salon in MVP │
  │ vs botox  │ │ 5 months    │ │             │ │ Vizag      │ │ Colony       │
  │ ~1,308 w  │ │ ~1,280 w    │ │ ~1,362 w    │ │ ~1,235 w   │ │ ~1,397 w     │
  │ MOFU      │ │ TOFU/MOFU   │ │ MOFU        │ │ BOFU       │ │ BOFU/local   │
  └───────────┘ └─────────────┘ └─────────────┘ └────────────┘ └──────────────┘
```

**Why each support exists:**

| Support | Reasons it exists | How it links up |
|---|---|---|
| 1. Keratin vs smoothening vs botox | Customers cannot choose between three similar services — this is the #1 pre-booking confusion. High search volume, weak local competition, and it maps directly to three services the studio sells. | Links to pillar twice; links to Support 04 (cost) for the price comparison |
| 2. How to make keratin last | The biggest post-purchase complaint is "it only lasted three weeks". Owning this query builds authority and reduces refund conversations. Informational traffic that converts later. | Links to pillar twice; links to Support 02's aftercare sibling (Support 04 for product cost) |
| 3. Does keratin damage hair? | The single biggest objection, and the one competitors answer dishonestly. An honest answer here creates the trust that converts everywhere else. | Links to pillar twice; links to Support 01 (to help them choose the gentler option) |
| 4. Keratin cost in Visakhapatnam | Highest commercial intent in the cluster. Almost nobody publishes real prices — the biggest content gap found in competitor research. Often out-converts the pillar. | Links to pillar twice; links to Support 03 (why the cheaper option isn't cheaper) |
| 5. Choosing a salon in MVP Colony | Captures "near me" and area searches the topic-led pillar cannot. Also passes local relevance signals to the whole cluster. | Links to pillar twice; links to Support 04 (what local prices look like) |

**Phase 2 (recommended, not in this delivery):** a second cluster around bridal — pillar "Bridal Makeup & Pre-Bridal Packages in Visakhapatnam" + supports (timeline, cost, choosing an artist, trial guide, pre-bridal skin prep). Same architecture, higher ticket value. Publish Aug–Sep ahead of the wedding season.

---

## 3. Cannibalisation check

| Article | Primary keyword | Would it satisfy the same query as another article? | Verdict |
|---|---|---|---|
| Pillar | keratin treatment in visakhapatnam | No — it's the broad commercial hub | ✅ Safe |
| S1 | keratin vs smoothening vs hair botox | No — comparison intent, not "find a service" | ✅ Safe |
| S2 | how long does keratin last | No — informational, post-decision | ✅ Safe |
| S3 | does keratin damage hair | No — objection/safety intent | ✅ Safe |
| S4 | keratin treatment cost in visakhapatnam | **Closest risk to the pillar.** Pillar covers cost in one section; S4 owns cost entirely | ⚠️ Managed — see note |
| S5 | hair salon in mvp colony visakhapatnam | No — local/place intent, not service intent | ✅ Safe |

**The one risk, and how it's handled:** the pillar and the cost article could compete on "keratin cost in Visakhapatnam". Resolution: the **pillar keeps one short cost table and links out with the anchor "full keratin cost breakdown"**; the **cost article owns the price topic in depth and never targets the pillar's phrase**. The pillar targets *"keratin treatment in visakhapatnam"* only — never *"cost"* in its title or H1. In Search Console, monitor which page ranks for the cost query and consolidate if they swap.

**Rules applied:** one primary keyword per page · no singular/plural duplicates · no two pages answering the same question · the pillar targets commercial intent, not curiosity.

---

## 4. Internal link matrix

| From ↓ / To → | Pillar | S1 compare | S2 aftercare | S3 damage | S4 cost | S5 local |
|---|---|---|---|---|---|---|
| **Pillar** | — | ✅ | ✅ | ✅ | ✅ | ✅ |
| **S1 Comparison** | ✅✅ | — | — | ✅ | ✅ | — |
| **S2 Aftercare** | ✅✅ | — | — | ✅ | ✅ | — |
| **S3 Damage** | ✅✅ | ✅ | — | — | — | — |
| **S4 Cost** | ✅✅ | ✅ | ✅ | — | — | ✅ |
| **S5 Local** | ✅✅ | — | — | — | ✅ | — |

✅✅ = two links required (one in the first 150 words, one in the closing section) · ✅ = one contextual link

**Total internal links: 15.** Every support reaches the pillar; the pillar reaches every support; no orphans in either direction.

**Anchor text rules used:**
- Use descriptive, varied anchors — never "click here" or "read more".
- Use the target page's primary keyword or a close natural variant as the anchor at least once.
- Vary the second anchor: "our full keratin treatment guide", "what the treatment involves", "how we handle damaged hair".
- Never link the same anchor text twice to the same page from one article.

**Full anchor-text assignments:** see `internal-link-map.md`.

---

## 5. Priority order

| Rank | Article | Business value | Intent | Effort | Why this order |
|---|---|---|---|---|---|
| 1 | **S4 — Cost** | H | BOFU | Low | Highest intent, biggest competitor gap, converts immediately, and it's the easiest win |
| 2 | **Pillar** | H | MOFU | High | The hub everything else links into; publish second so the cost article already has somewhere to link up to |
| 3 | **S3 — Objection** | H | MOFU | Medium | Answers the biggest blocker; strengthens trust for the whole cluster |
| 4 | **S1 — Comparison** | H | MOFU | Medium | Covers three services at once; supports conversion of undecided buyers |
| 5 | **S5 — Local** | H | BOFU/local | Low–Medium | Area searches; reinforces local pack relevance |
| 6 | **S2 — Aftercare** | M | TOFU | Low | Authority and retention; least commercial, so it goes last |

**Publishing schedule at 2 articles/month** (matches the client's review capacity):

| Month | Articles |
|---|---|
| Month 1 | S4 (cost) · Pillar |
| Month 2 | S3 (objection) · S1 (comparison) |
| Month 3 | S5 (local) · S2 (aftercare) |

**Why not all six at once:** publishing beyond the owner's review capacity is precisely the pattern Google's scaled-content-abuse policy targets, and it gives you no time to read Search Console between articles. Six articles over three months, each with first-hand detail, is strictly better than six in one week.

---

## 6. Strategy summary (plain language, for the business owner)

> Your customers search in two ways: they ask *"keratin treatment in Visakhapatnam"* and *"how much does keratin cost"* when they're ready to buy, and they ask *"does keratin damage hair"* and *"how long does it last"* when they're unsure. Right now, no salon in your area answers either set properly. They list services and hide prices.
>
> So we're building six pages that work as one system. One main article covers keratin properly — the process, the honest price range, how long it lasts, and who it isn't right for. Five smaller articles each own one question your customers already ask, and every one of them links back to the main article. Google sees a site that covers a topic deeply, and readers get their answer without calling you first.
>
> We publish two a month, starting with the cost article, because that's what people search when they're ready to spend. In about three months you should see these pages showing up in search — impressions first, then positions, then enquiries. One extra keratin booking covers the whole cluster.
