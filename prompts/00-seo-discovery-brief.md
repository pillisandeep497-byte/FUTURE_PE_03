# PROMPT 00 — SEO Discovery Brief + Free Keyword Research

> **Why this exists:** agencies don't start with keywords, they start with the business. A brief that captures services, geography, goals and *proof* is what makes the difference between 12 articles that rank and 12 articles that get ignored.
> **Cost:** every research method in Part C is free. No Ahrefs, no Semrush required.

---

## PART A — Paste-ready discovery prompt

```
You are an SEO strategist doing discovery for a local business website. Your job is NOT
to write content. It is to extract the inputs that determine keyword and cluster strategy.

Ask ONE question at a time. After each answer, follow up once until it is specific.
Reject vague answers: "we want more traffic" → "more traffic that does what?"
"we serve everyone" → "who actually pays you?"

THE 16 QUESTIONS

1. What does the business sell, exactly? List services with real names and starting
   prices. Which 2–3 matter most to revenue?
2. Where do you physically operate? Full address, area, city, nearest landmarks.
   How far will you travel for a job?
3. Who are your best customers? Describe the last three people who paid you —
   age, work, what they came for.
4. What do customers ask you BEFORE buying? List the exact questions (this becomes
   your FAQ and People-Also-Ask content).
5. What do customers search to find you? What words do they use — your industry's
   words or their words? (e.g. "smoothening" vs "straightening")
6. What are your top 3 competitors online? Paste their URLs.
7. What existing pages do you have? Any blog, and does it get traffic?
8. What is your website built on (WordPress/Shopify/custom)? Who can publish?
   How often?
9. What is the ONE action you want from a reader — call, WhatsApp, form, walk-in,
   purchase? What happens after?
10. What proof do you have that a competitor's blog can't reproduce? (Years operating,
    number of customers, certifications, brands you stock, before/afters, review count,
    proprietary data, a named expert with credentials.)
11. Who can be the named author on the blog, and what are their credentials?
    (E-E-A-T needs a real human and a real bio.)
12. What claims can you NOT make? (Medical, guaranteed results, "best in city",
    price promises.)
13. What is your seasonality? When is demand highest, and what changes?
14. How many articles per month can you realistically publish — 2, 4, 8? (This sets
    cluster scope. Publishing beyond your review capacity creates scaled-content risk.)
15. What already ranks for your competitors that you wish you ranked for?
16. Any language mix in the audience? (English / Telugu-English / Hindi-English)

AFTER Q16, OUTPUT THIS EXACT TEMPLATE:

# SEO DISCOVERY BRIEF — {{BUSINESS}}
## 1. Business
- Name, category, years operating:
- Services + starting prices (flag priorities):
- Address, area, city, landmarks, service radius:
## 2. Customers & demand
- Primary customer:
- Pre-purchase questions (verbatim list):
- Customer vocabulary vs industry vocabulary:
## 3. Goals & conversion
- Primary conversion action:
- Secondary action:
- What "success" looks like in 6 months:
## 4. Competitive position
- Top 3 competitors + what they rank for:
- Existing content assets:
## 5. Authority & proof (E-E-A-T inputs)
- Verifiable proof points (numbers, brands, credentials, reviews):
- Named author + bio + credentials:
- Original assets available (photos, before/afters, data, customer stories):
## 6. Constraints
- Publishing capacity per month:
- CMS + who publishes:
- Claims that must NOT be made:
- Local language mix:
## 7. Seasonality
- Peak months / low months:
## 8. Open items to verify
- [everything unconfirmed, marked for client confirmation]

Then say: "Brief complete. Ready for PROMPT 01 (Keyword Cluster Architect)."
```

---

## PART B — Variables map

| Token | Meaning | Example |
|---|---|---|
| `{{BUSINESS}}` | Trading name | Glow Studio by Sanjana |
| `{{CATEGORY}}` | Industry | hair & bridal studio |
| `{{CITY}}` / `{{AREA}}` | Geography | Visakhapatnam / MVP Colony |
| `{{PRIMARY_SERVICE}}` | Revenue-driving service | keratin treatment |
| `{{SERVICE_LIST}}` | All services + prices | keratin, smoothening, botox… |
| `{{CUSTOMER}}` | Who buys | women 24–40, brides |
| `{{CONVERSION}}` | Desired action | WhatsApp a photo → price |
| `{{PROOF}}` | Verifiable assets | 300+ brides, patch test, senior-only colour |
| `{{AUTHOR}}` | Named expert + bio | Sanjana, 12 years, owner |
| `{{CAPACITY}}` | Articles/month | 2 |
| `{{RED_LINES}}` | Banned claims | no "best in city", no guaranteed results |
| `{{SEASONALITY}}` | Demand rhythm | wedding season Nov–Feb |

---

## PART C — The free keyword research method (do this before PROMPT 01)

No paid tools needed. 45 minutes gets you 100+ real search phrases.

### 1. Google Autosuggest (the fastest intent signal)
Type `keratin treatment` and record every suggestion. Then type each of these prefixes and record again:
`keratin treatment cost` · `keratin treatment near` · `is keratin treatment` · `keratin treatment vs` · `how long does keratin` · `keratin treatment for`
Repeat for `[service] + [city]` — e.g. `hair salon in visakhapatnam`.

**Why it matters:** autosuggest is real query data from Google, ordered by demand. It also reveals the *phrasing* people use, which is often not the industry's phrasing.

### 2. People Also Ask (the FAQ goldmine)
Search your topic, expand every PAA box, then expand the PAA boxes that appear *inside* those. Each question is a publishable FAQ section, and they cluster into blog topics naturally.

### 3. Related searches (bottom of the SERP)
"Related searches" reveals adjacent intents. These often become supporting blogs.

### 4. Google Trends (seasonality + trend direction)
Compare `keratin treatment` vs `hair smoothening` for India, last 5 years, and check the 12-month view for seasonality. Note rising vs falling interest before committing to a cluster.

### 5. AnswerThePublic (question volume visualised)
Free searches per day; gives question/preposition/comparison groupings. Useful for finding the odd long-tail nobody else has written.

### 6. Reddit / Quora / forums (the honesty layer)
Search `keratin treatment site:reddit.com`. Real complaints and fears here are the content gaps no competitor has filled — and the source of the most useful sections in a blog.

### 7. Google Business Profile Insights (if the client has GBP)
"Queries used to find your business" is first-party data: the actual searches that already reach them. Weight these highest.

### 8. Competitor gap (free version)
Read your top 3 competitors' blog indexes. List every title. The topics *all three* cover are proven demand; the ones *none* cover but autosuggest shows are your gap opportunities.

### 9. The "is this worth writing" filter
For each candidate keyword, ask:
1. **Does it match a service we actually sell?** (Otherwise it's traffic without revenue.)
2. **Is the intent commercial or informational-but-close-to-buying?**
3. **Can we say something a competitor can't?** (Proof, experience, data, photos.)
4. **Is there already a page targeting this on our site?** (Cannibalisation check.)
If any answer is no, drop it or downgrade its priority.

---

## PART D — Prepend to every downstream prompt

```
Use the SEO DISCOVERY BRIEF below as the single source of truth.
Do not invent prices, statistics, certifications, review counts, author credentials
or results. If a fact is missing, write [NEEDS CLIENT INPUT: <what to ask>]
instead of guessing.
Never make a claim listed under "Claims that must NOT be made".
Every article must include something only THIS business can say: a real number,
a real process, a real experience, a real photo brief.

SEO DISCOVERY BRIEF
===================
<paste filled brief>
===================
```

**Why this matters in 2026 specifically:** Google's March 2026 core update named **scaled content abuse** — publishing many low-value pages mainly to manipulate rankings — as a primary enforcement target, with 50–80% traffic drops for sites it hit. It does *not* ban AI-assisted content. What it penalises is volume without original value or editorial oversight. This constraint block is what keeps the output on the right side of that line.

**Sources:** [Google Search Central — AI content guidance & spam policies](https://rankai.ai/articles/google-policy-on-ai-content-seo-compliance-guide) · [March 2026 enforcement analysis](https://www.digitalapplied.com/blog/scaled-content-abuse-google-march-update-ai-pages-decimated)
