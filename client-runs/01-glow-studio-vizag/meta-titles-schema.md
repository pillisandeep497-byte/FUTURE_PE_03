# Meta Titles, Descriptions, Slugs & Schema — Keratin Cluster

All character counts verified with a counter, not by eye.

---

## 1. Titles, metas and slugs

### Pillar
- **Title tag (58):** `Keratin Treatment in Visakhapatnam: Cost, Process & Results`
- **Meta description (152):** `What keratin treatment in Visakhapatnam really costs, how long it takes, how long it lasts, and who shouldn't get it. Honest advice from MVP Colony.`
- **Slug:** `/blog/keratin-treatment-visakhapatnam`
- **H1:** `Keratin Treatment in Visakhapatnam: Cost, Process, Results & Honest Advice`

### S1 — Comparison
- **Title tag (57):** `Keratin vs Smoothening vs Hair Botox: Which Do You Need?`
- **Meta description (149):** `Keratin smooths, smoothening straightens, botox repairs. Here's which one suits your hair — with costs, how long each lasts, and who should avoid each.`
- **Slug:** `/blog/keratin-vs-smoothening-vs-hair-botox`
- **H1:** `Keratin vs Smoothening vs Hair Botox: Which One Do You Actually Need?`

### S2 — Aftercare
- **Title tag (55):** `How to Make a Keratin Treatment Last 5 Months, Not 3`
- **Meta description (147):** `Keratin lasts 3–5 months if you do three things right. The washing routine, products to avoid and the mistakes that strip a treatment in weeks.`
- **Slug:** `/blog/how-to-make-keratin-last-longer`
- **H1:** `How to Make a Keratin Treatment Last 5 Months Instead of 3`

### S3 — Objection
- **Title tag (54):** `Will Keratin Damage My Hair? An Honest Answer`
- **Meta description (150):** `Keratin usually damages hair when a salon skips a step or treats unsuitable hair. Here's what actually goes wrong, and the seven questions to ask before booking.`
- **Slug:** `/blog/does-keratin-damage-hair`
- **H1:** `Will Keratin Damage My Hair? An Honest Answer`

### S4 — Cost
- **Title tag (59):** `Keratin Treatment Cost in Visakhapatnam: Full Price Guide`
- **Meta description (148):** `Keratin treatment in Visakhapatnam costs ₹4,500–₹8,000, depending on length and thickness. See what changes the price and what the cheap option really costs.`
- **Slug:** `/blog/keratin-treatment-cost-visakhapatnam`
- **H1:** `Keratin Treatment Cost in Visakhapatnam: What You're Actually Paying For`

### S5 — Local
- **Title tag (58):** `How to Choose a Hair Salon in MVP Colony, Visakhapatnam`
- **Meta description (151):** `Six things that separate good MVP Colony salons from the rest, area price ranges, red flags, and the questions to ask before booking a colour or keratin service.`
- **Slug:** `/blog/hair-salon-mvp-colony-visakhapatnam`
- **H1:** `How to Choose a Hair Salon in MVP Colony, Visakhapatnam`

**Rules applied:** keyword first · brand name omitted from blog titles (better CTR on informational queries) · no clickbait · no "best/#1" · counts within Google's display limits (60 / 155).

---

## 2. Schema plan

| Article | Schema types | Why |
|---|---|---|
| Pillar | `Article` + `FAQPage` + `Service` + `LocalBusiness` | Article for the blog, FAQPage for the PAA block, Service for the specific service, LocalBusiness for local relevance |
| S1 Comparison | `Article` + `FAQPage` | Comparison content; FAQ block present |
| S2 Aftercare | `Article` + `FAQPage` + `HowTo` * | HowTo only if the steps are presented as an ordered procedure with clear steps |
| S3 Damage | `Article` + `FAQPage` | Objection content; FAQ block present |
| S4 Cost | `Article` + `FAQPage` + `Service` | Publish real prices in `offers` — this is what wins price queries |
| S5 Local | `Article` + `FAQPage` + `LocalBusiness` | Local article, strongest place for the full LocalBusiness entity |
| Site-wide | `BreadcrumbList` | Every blog page |

`*` Google has reduced HowTo rich results in search. Keep the structured data for semantic clarity, but do not expect a rich result from it.

**Never do:** fake `AggregateRating` or `Review` markup without genuine, displayed, verifiable reviews. It's a policy violation and a manual-action risk.

---

## 3. Ready-to-paste JSON-LD

### Pillar — Article + FAQPage + Service + LocalBusiness

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@graph": [
    {
      "@type": "Article",
      "@id": "{{PILLAR_URL}}#article",
      "headline": "Keratin Treatment in Visakhapatnam: Cost, Process, Results & Honest Advice",
      "description": "What keratin treatment in Visakhapatnam costs, how long it takes and lasts, and who should not get it.",
      "author": { "@type": "Person", "name": "Sanjana", "jobTitle": "Owner and Senior Stylist", "url": "{{AUTHOR_PAGE_URL}}" },
      "publisher": { "@type": "Organization", "name": "Glow Studio by Sanjana", "logo": { "@type": "ImageObject", "url": "{{LOGO_URL}}" } },
      "datePublished": "{{PUBLISHED}}",
      "dateModified": "{{UPDATED}}",
      "image": ["{{HERO_IMAGE_URL}}"],
      "mainEntityOfPage": { "@type": "WebPage", "@id": "{{PILLAR_URL}}" },
      "about": { "@type": "Service", "name": "Keratin treatment" }
    },
    {
      "@type": "Service",
      "@id": "{{PILLAR_URL}}#service",
      "name": "Keratin treatment",
      "serviceType": "Hair keratin treatment",
      "provider": { "@id": "{{HOME_URL}}#localbusiness" },
      "areaServed": { "@type": "City", "name": "Visakhapatnam" },
      "offers": {
        "@type": "Offer",
        "priceCurrency": "INR",
        "priceSpecification": {
          "@type": "PriceSpecification",
          "minPrice": "4500",
          "maxPrice": "8000",
          "priceCurrency": "INR"
        },
        "availability": "https://schema.org/InStock",
        "url": "{{PILLAR_URL}}"
      }
    },
    {
      "@type": "FAQPage",
      "@id": "{{PILLAR_URL}}#faq",
      "mainEntity": [
        { "@type": "Question", "name": "How much does keratin cost in Visakhapatnam?",
          "acceptedAnswer": { "@type": "Answer", "text": "Usually ₹4,500 to ₹8,000 depending on hair length, thickness and product range. At Glow Studio it starts at ₹4,500, confirmed in writing after a free strand assessment." } },
        { "@type": "Question", "name": "How long does a keratin treatment take?",
          "acceptedAnswer": { "@type": "Answer", "text": "Three to four hours for most hair lengths, including wash, application, drying and sealing." } },
        { "@type": "Question", "name": "Will keratin damage my hair?",
          "acceptedAnswer": { "@type": "Answer", "text": "Not when applied correctly on suitable hair. Damage typically follows a skipped clarifying wash or sealing step, or treatment on already over-processed hair." } },
        { "@type": "Question", "name": "How long does a keratin treatment last?",
          "acceptedAnswer": { "@type": "Answer", "text": "Usually three to five months, depending on hair type and aftercare. Daily washing with sulfate shampoo shortens it to six to eight weeks." } },
        { "@type": "Question", "name": "Can I wash my hair after keratin?",
          "acceptedAnswer": { "@type": "Answer", "text": "Not for 48 to 72 hours. Afterwards, use sulfate-free shampoo and wash two to three times a week." } },
        { "@type": "Question", "name": "Is keratin treatment safe?",
          "acceptedAnswer": { "@type": "Answer", "text": "Professional keratin is widely used and considered safe when applied correctly to suitable hair. Mention any scalp condition, pregnancy or known sensitivity before booking." } }
      ]
    }
  ]
}
</script>
```

### S5 — LocalBusiness block (also place site-wide in the footer)

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "BeautySalon",
  "@id": "{{HOME_URL}}#localbusiness",
  "name": "Glow Studio by Sanjana",
  "image": "{{STUDIO_PHOTO_URL}}",
  "url": "{{HOME_URL}}",
  "telephone": "{{PHONE}}",
  "priceRange": "₹₹",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "1st Floor, above Sri Sai Bakery, MVP Colony Main Road, Sector 4",
    "addressLocality": "Visakhapatnam",
    "addressRegion": "Andhra Pradesh",
    "postalCode": "530017",
    "addressCountry": "IN"
  },
  "geo": { "@type": "GeoCoordinates", "latitude": "{{LAT}}", "longitude": "{{LNG}}" },
  "areaServed": [
    { "@type": "City", "name": "Visakhapatnam" },
    { "@type": "Place", "name": "MVP Colony" },
    { "@type": "Place", "name": "Seethammadhara" },
    { "@type": "Place", "name": "Gajuwaka" }
  ],
  "openingHoursSpecification": [{
    "@type": "OpeningHoursSpecification",
    "dayOfWeek": ["Monday","Tuesday","Wednesday","Thursday","Friday","Saturday","Sunday"],
    "opens": "10:00", "closes": "20:30"
  }],
  "sameAs": ["{{GOOGLE_BUSINESS_PROFILE_URL}}", "{{INSTAGRAM_URL}}"],
  "hasOfferCatalog": {
    "@type": "OfferCatalog",
    "name": "Hair and beauty services",
    "itemListElement": [
      { "@type": "Offer", "itemOffered": { "@type": "Service", "name": "Keratin treatment" },
        "priceSpecification": { "@type": "PriceSpecification", "minPrice": "4500", "maxPrice": "8000", "priceCurrency": "INR" } },
      { "@type": "Offer", "itemOffered": { "@type": "Service", "name": "Hair smoothening" },
        "priceSpecification": { "@type": "PriceSpecification", "minPrice": "3800", "maxPrice": "6500", "priceCurrency": "INR" } },
      { "@type": "Offer", "itemOffered": { "@type": "Service", "name": "Bridal HD makeup" },
        "priceSpecification": { "@type": "PriceSpecification", "minPrice": "18000", "priceCurrency": "INR" } }
    ]
  }
}
</script>
```

### Breadcrumb (all blog pages)

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "itemListElement": [
    { "@type": "ListItem", "position": 1, "name": "Home", "item": "{{HOME_URL}}" },
    { "@type": "ListItem", "position": 2, "name": "Blog", "item": "{{BLOG_URL}}" },
    { "@type": "ListItem", "position": 3, "name": "{{ARTICLE_H1}}", "item": "{{ARTICLE_URL}}" }
  ]
}
</script>
```

---

## 4. Technical checklist before publishing each article

- [ ] Slug short, lowercase, hyphenated, no dates
- [ ] Title tag ≤60 characters — **counted, not estimated**
- [ ] Meta description ≤155 characters — counted
- [ ] One H1 on the page; heading order H1 → H2 → H3, no skipped levels
- [ ] Canonical tag self-referencing
- [ ] Images: compressed to WebP, descriptive file names, alt text written for each
- [ ] Internal links present in the required count with the planned anchors
- [ ] External sources linked where claims are made
- [ ] JSON-LD added and validated in the Rich Results Test
- [ ] Author bio block present and linked to an author page
- [ ] Published + last-updated dates visible
- [ ] Added to the sitemap and resubmitted
- [ ] Indexing requested via URL Inspection
- [ ] Mobile check: table scrolls, no horizontal overflow, text readable
- [ ] WhatsApp CTA tested on a phone

---

## 5. Image briefs and alt text

| Article | Images needed | Alt text |
|---|---|---|
| Pillar | 1. Studio interior with chairs and window light · 2. Strand being checked between fingers · 3. Treatment applied section by section · 4. Finished smooth hair in daylight | `Keratin treatment salon in MVP Colony Visakhapatnam with styling chairs and morning light` · `Stylist checking hair strand elasticity before a keratin treatment` · `Keratin formula applied section by section to long dark hair` · `Smooth glossy hair after a keratin treatment in Visakhapatnam` |
| S1 | 1. Side-by-side: frizzy vs smoothed hair · 2. Three product ranges on the counter | `Comparison of frizzy hair and keratin-treated smooth hair` |
| S2 | 1. Sulfate-free shampoo on a shelf · 2. Silk pillowcase / styling setup | `Sulfate-free shampoo recommended after a keratin treatment` |
| S3 | 1. Hands holding two strands comparing damage · 2. Aftercare sheet being handed over | `Comparing damaged and healthy hair strands before a keratin treatment` |
| S4 | 1. Price being written on paper at the desk · 2. Studio price list (text in HTML, not an image) | `Stylist writing the final keratin treatment price before the service begins` |
| S5 | 1. Studio signboard from the street showing the bakery landmark · 2. Street view of MVP Colony Main Road | `Glow Studio entrance above Sri Sai Bakery on MVP Colony Main Road Visakhapatnam` |

**Rules:** real photos only — never stock images of a different salon. Every image original, compressed, and named descriptively (`keratin-treatment-mvp-colony-visakhapatnam.webp`) before upload.
