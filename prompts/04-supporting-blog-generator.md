# PROMPT 04 — Supporting Blog (Cluster) Generator

Six article types, each with a different job. Run this prompt once per support article — never batch them, or the cluster reads as six versions of one article (which is exactly what Google's scaled-content-abuse policy targets).

---

## The prompt

```
# ROLE
You are a content strategist writing a supporting article inside a cluster. Your
article has one job: rank for a specific long-tail query, be genuinely useful on its
own, and hand the reader to the pillar article when they're ready for the full picture.

# INPUTS
SEO DISCOVERY BRIEF: <paste>
PILLAR ARTICLE (title, URL, primary keyword): <paste>
THIS ARTICLE — type: {{TYPE}}, primary keyword: {{PRIMARY}}, word target: {{WORDS}}
SIBLING ARTICLES (for cross-linking, don't duplicate): <list titles + primary keywords>

# THE SIX SUPPORT TYPES

1. COMPARISON — "[X] vs [Y] vs [Z]"
   Structure: answer-first verdict (who each one is for) → comparison table →
   one H2 per option with what it does and who it suits → how a professional decides
   → cost comparison → FAQ → CTA.
   Rule: declare a real recommendation. "It depends" articles don't rank or convert.

2. OBJECTION — "Will [X] damage/hurt/is [X] worth it?"
   Structure: answer-first (direct yes/no/caveat) → what actually goes wrong →
   how to tell if you're at risk → what a responsible provider does differently
   → what to do if you've already had a bad experience → FAQ → CTA.
   Rule: never dismiss the fear. Validate it with evidence, then resolve it with process.

3. HOW-TO / MAINTENANCE — "How to make [X] last / prepare for [X]"
   Structure: answer-first (the 3 things that matter most) → numbered routine with
   timings → what to avoid and why → common mistakes → a simple checklist →
   FAQ → CTA.
   Rule: every step must be actionable today, with no purchase required for step 1.

4. COST — "[Service] cost/price in [city] — what you're actually paying for"
   Structure: answer-first price range → what changes the price (table) →
   cheap vs mid vs premium, honestly → what's included at each level →
   hidden costs to ask about → how to get an accurate quote → FAQ → CTA.
   Rule: publish real ranges. A cost article with no numbers is worthless and
   will not rank against one that has them.

5. LOCAL — "[Service] in [area/city] / how to choose a [category] in [city]"
   Structure: answer-first on what to look for → a 6–8 point checklist of what good
   looks like (with local context: travel, parking, water quality, humidity, season)
   → red flags → what to ask on the phone → how pricing works in this city →
   FAQ → CTA with landmark-level detail.
   Rule: this must contain genuinely local content (real landmarks, local conditions,
   local pricing norms). A template with the city name swapped in is a doorway page
   and is explicitly penalised — do not produce one.

6. FAQ / QUESTION HUB — "Your top questions about [topic], answered"
   Structure: 8–12 questions, each answered in 40–60 words, grouped by theme
   (price / safety / process / aftercare) → a short intro explaining who this is for
   → internal links to the deeper articles for each theme.
   Rule: keep answers short enough to be snippet-lifted; link out for depth.

# TASK
Write the complete article for the type above. Include:
- H1, meta title (≤60 chars, count it), meta description (≤155 chars, count it),
  URL slug
- Author byline + credential, published + updated dates
- The structure specified for this type
- 2 links UP to the pillar (one in the first 150 words, one in the closing section)
  with descriptive anchor text, plus 1 link to a sibling article
- One FAQ block of 4–6 questions with FAQPage schema after the body
- A closing CTA: specific action + what it costs to ask + what happens next
- "PHOTO BRIEF" for 2–4 original images with alt text
- "WORD COUNT" — the actual number

# HARD CONSTRAINTS
- 700–1,300 words. Shorter and complete beats longer and padded.
- The primary keyword must NOT be the same as any sibling or the pillar.
- Do not repeat the pillar's structure. A support article that mirrors the pillar
  creates cannibalisation instead of support.
- Answer-first in the first 60 words.
- At least 2 first-hand signals: a real number, a real process, a real local detail.
- One honest limitation or caveat.
- No claim without a source or a flag. Never invent statistics, review counts or
  before/after results.
- If the article would be identical to a competitor's except for the business name,
  the article has failed — add experience-specific content.

# BANNED
Same banned list as PROMPT 03 (in today's fast-paced world, unlock, delve, elevate,
game-changer, must-have, one-stop shop, seamless, hassle-free, in conclusion,
everything you need to know, etc.).
Also banned: repeating the pillar's intro, generic definitions that could come from
a dictionary, and "consult a professional" as a substitute for an actual answer.

# OUTPUT FORMAT
Markdown, publish-ready. Then FAQPage JSON-LD, then the photo brief and word count.

# SELF-CHECK
1. Does this article stand alone for someone who never reads the pillar?
2. Does it link up naturally, or does the link feel bolted on?
3. Is the primary keyword distinct from every sibling?
4. Would this article be useful to a reader who never buys?
5. Does it contain something a competitor can't copy?
End with "--- SUPPORT ARTICLE READY ---" and scores (Intent match, Usefulness,
Internal linking, Originality, Snippet-readiness) each 1–5.
```

---

## Support-article quality ladder

| Level | What it looks like | Rank outcome |
|---|---|---|
| **1. Thin** | Definition, generic advice, no numbers, no experience | Indexed, never ranks. Risks scaled-content classification if repeated at volume |
| **2. Competent** | Complete, accurate, sourced, well-structured | Ranks on long-tail with low competition |
| **3. Useful** | Adds real prices, timelines, process and local detail | Ranks and converts; earns links |
| **4. Distinct** | Contains information only this business can provide — its prices, its refusals, its data | Ranks, converts, and becomes the page competitors can't out-write |

Aim for level 3–4 on every article, and publish fewer articles if that's what it takes.

## Cluster hygiene rules

1. **One primary keyword per article.** Two articles for one query = one article wasted.
2. **Every support links up twice.** Otherwise the cluster has no topology, just a list.
3. **Stagger publishing.** One article every 2–3 weeks beats four in one week — it reads as a living site, and it gives you time to check each one in Search Console before the next.
4. **Update, don't multiply.** When a support article starts ranking, expand it rather than writing a new article on the same theme. Consolidation beats proliferation.
5. **Kill weak pages.** If a page has had zero impressions after 4 months, either rewrite it or delete and redirect. Thin pages drag on the whole site.
