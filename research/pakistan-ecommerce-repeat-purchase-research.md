# Pakistan E-Commerce Product Research: Repeat-Purchase Business Models for Meta Ads

**Prepared:** September 19, 2026
**Scope:** Identify consumable/replenishable product niches for a small Pakistani e-commerce brand built on Meta/Facebook/Instagram ads, COD + online payments.

**Methodology note (read first):** This report combines (1) live Meta Ad Library queries (via API, pulled 2026-09-19, filtered to ads currently reaching Pakistan) used as a real-time demand/competition proxy, (2) Google web-search-surfaced market reports, news coverage, and Daraz.pk listings, and (3) explicit modeling for numbers that cannot be observed directly (costs, CAC, conversion rates). Google Trends itself could not be queried directly (it requires a JavaScript browser session my tools cannot render), so Meta Ad Library's `estimated_total_count` and Daraz category presence are used as demand/competition proxies instead — this is a real limitation, stated once here rather than repeated on every line. Every table below marks numbers as **FACT** (sourced, verifiable), **ESTIMATE** (modeled from sourced inputs, shown with method), or **ASSUMPTION** (reasonable but unverified judgment call). Where I could not find or verify something, I say so explicitly rather than inventing a figure. Full citations are in the **SOURCES** section.

---

## EXECUTIVE SUMMARY

Pakistan's e-commerce market is genuinely growing (~13.2%/year, ~$14.1B by 2025 trending to ~$20.4B by 2029) with **grocery and beauty flagged as the fastest-growing categories** and Daraz's own data pointing to skincare/personal-care as the highest sales-velocity segment [1][4][5]. But most "winning products" content aimed at Pakistani sellers is gadget/novelty-driven — the opposite of what you asked for.

I pulled live Meta Ad Library data for ~15 candidate niches (real ads currently running against Pakistan, Sept 2026) rather than guessing. Two categories I expected to be viable turned out to be traps, confirmed by evidence, not assumption:

- **Whey protein/supplements** has enormous real Meta ad activity (294 active ads, real spenders like Styx Nutrition and King Nutritions) — but Meta's own Health & Wellness policy imposes heavy restrictions (no before/after, no disease-cure claims, 64%+ of supplement accounts face review) [29][30], and you explicitly asked to avoid regulatory/medical-claim exposure. **Eliminated.**
- **Household cleaners / detergent** looked "obviously consumable," but Unilever alone runs 258,000 retail touchpoints in Pakistan and Harpic holds 80%+ of the branded toilet-cleaner segment [20][21]; the Meta Ad Library shows essentially zero genuine D2C challenger activity in this space. A small brand cannot out-distribute or out-price incumbents sold in every corner shop. **Eliminated.**

After generating 33 ideas and filtering hard against your criteria (see Tables 1–2), four categories survive with real, verifiable demand **and** genuine Meta-ads-native competitors already proving the model works:

1. **Premium breathable sanitary pads** — highest, most predictable repeat cycle (~4 weeks) of anything tested; a real local challenger (**Butterfly Pakistan**, 75K Instagram followers) has documented success taking share from Always using exactly this playbook [17][18][19].
2. **Lightweight, no-white-cast sunscreen for South Asian skin** — the single largest demand signal found (2,159 active Meta ads reaching Pakistan), with real, well-reviewed local brands (Oribelle, De Rien) proving the format works [source: live Meta Ad Library query].
3. **Bakhoor/oud/attar home-fragrance ritual kits** — smaller but real and *not* oversaturated (31 active ads vs. sunscreen's 2,159), the best margin structure of anything tested, and the strongest brand/gifting story.
4. **Cat food/litter/treats replenishment** — real dedicated Pakistani sellers (Petlife.pk, Meowmarket.pk) with genuine multi-SKU pricing and a growing urban pet-owner base, but the weakest unit economics of the four once shipping weight and Whiskas-anchored price ceilings are modeled honestly.

**The unit economics section is the most important part of this report, and it is not flattering.** Using Pakistan's own sourced numbers — COD RTO averaging 18–20% nationally [24][25][26], Meta cost-per-lead of PKR 281–845 [28] — modeled first-order contribution profit is **negative or barely positive for all four categories at base-case assumptions.** This is not a reason to abandon the idea; it's the normal, well-documented shape of COD-driven Meta ads businesses in Pakistan: **you lose money or break even on order #1, and the entire business case depends on repeat orders, which carry near-zero acquisition cost.** Bakhoor has the best-cushioned economics of the four; cat-care bundles anchored on food/litter have the worst (thin margin + heavy shipping), and only work if the *acquisition* SKU is treats/accessories rather than staple food.

My evidence-weighted recommendation (Table 6 scoring matrix): **Sanitary Pads (7.7/10) > Sunscreen (7.4/10) > Bakhoor (7.15/10) > Cat Care (7.05/10)** — a near-four-way tie. For a first-time founder with **genuinely small capital**, I'd sequence differently than the pure score: **start with Bakhoor** (lowest sourcing complexity, lowest regulatory friction, least saturated, best margin cushion against RTO/CAC shocks), treat **Sanitary Pads** as the highest-conviction second product once you have working capital and courier/RTO discipline, and be honest that **Sunscreen** requires the sharpest possible differentiation angle to avoid being drowned out by De Rien's ad spend.

---

## TABLE 1 — 30+ INITIAL PRODUCT IDEAS

Evidence tier: 🟢 = validated with live Meta Ad Library data + web sources · 🟡 = partial/weak evidence found · 🔴 = insufficient evidence found (said so rather than invented)

| # | Product / Niche | Main Customer | Why They'd Reorder | Repurchase Interval | Price Range (PKR) | Verdict |
|---|---|---|---|---|---|---|
| 1 | No-white-cast lightweight sunscreen (desi skin) 🟢 | Urban women 18–40, skincare-aware | Used up every day, sun exposure year-round | 4–8 weeks | 800–2,500 | **ADVANCE** |
| 2 | Vitamin C / niacinamide face serum 🟡 | Skincare-conscious women | Daily use, bottle empties | 6–10 weeks | 900–2,800 | Cut — brutally crowded, cosmetic-claim scrutiny, hard to differentiate |
| 3 | Face sheet masks / mask bundles 🔴 (ad-library query returned only unrelated drama-app noise) | Young women, gifting | Single-use, buy in packs | 2–4 weeks | 600–1,800/box | Cut as standalone — fold into skincare brand's ladder, not a brand on its own |
| 4 | Acne spot patches 🟡 | Teens/young adults | Used per breakout | Irregular | 400–900 | Cut — Meta scrutinizes "acne" as a health condition; irregular usage hurts predictability |
| 5 | Face wash / cleanser 🔴 | Mass market | Daily use | 6–8 weeks | 300–900 | Cut — Unilever/P&G (Pond's, Clean & Clear) own this shelf at low price points |
| 6 | Herbal hair oil (onion/castor) 🔴 | Mass market women | Daily/weekly use | 4–6 weeks | 300–700 | Cut — oversaturated commodity; identical product sold everywhere cheaper |
| 7 | Anti-hair-fall serum/tonic 🟡 | Men & women, hair loss concern | Daily use | 6–8 weeks | 800–2,000 | Cut — medical-claim adjacent ("hair fall" = health condition), high ad rejection risk |
| 8 | Henna / hair color 🟢 (only 4 active ads found) | Mass market | Monthly touch-up | 4–6 weeks | 150–400 | Cut — near-zero genuine D2C Meta activity found; commodity, bought at kiryana stores |
| 9 | Teeth-whitening kit 🟡 | Young adults | Repeat treatments | 4–8 weeks | 1,200–3,000 | Cut — cosmetic/dental claim risk, needs real user education, ad rejection risk |
| 10 | Herbal/miswak toothpaste 🔴 | Mass market | Daily use | 6–8 weeks | 200–450 | Cut — no real D2C Meta signal found; Colgate/Sensodyne retail dominance |
| 11 | **Bakhoor / oud / attar ritual kits** 🟢 | Homeowners, gifting occasions | Cones/resin consumed with use | 4–6 weeks | 1,200–4,000 | **ADVANCE** |
| 12 | Soy / scented candles 🟢 (real: Nirvana Candle Co.) | Home-decor conscious urban women | Burns down with use | 4–6 weeks | 1,000–2,500 | Keep as **line extension** of #11, not core SKU — melt/breakage risk in transit (see Risks) |
| 13 | Perfume / body-spray bundle sets 🟢 | Broad, gifting-heavy | Bottle empties | 6–10 weeks | 600–2,500 | Keep in Top 10 — real but crowded (Admiral, RIOS already own budget tier) |
| 14 | Car air-freshener refills 🟢 (Admiral etc. sell as add-on) | Car owners | Refill every few weeks | 3–5 weeks | 150–400 | Cut — too low AOV/brand ceiling to be a standalone brand |
| 15 | Reed diffuser / wardrobe sachets 🔴 | Niche home-decor buyers | Refill oil | 6–8 weeks | 800–1,500 | Cut — insufficient evidence of any real Pakistani Meta activity |
| 16 | **Cat food / litter / treats replenishment** 🟢 | Urban cat owners | Consumable, runs out on schedule | 3–4 weeks | 800–4,000+ | **ADVANCE** |
| 17 | Dog food/supplies 🟡 | Smaller dog-owning segment | Same mechanic as #16 | 3–4 weeks | 1,000–4,000 | Deprioritize — smaller Pakistani dog-owning base than cat; weaker evidence found |
| 18 | Pet grooming wipes/shampoo 🟡 | Pet owners | Replenished monthly | 4–6 weeks | 500–1,200 | Fold into #16's product ladder as upsell, not standalone |
| 19 | **Premium breathable sanitary pads** 🟢 | Women 13–45 | Menstrual cycle | ~4 weeks | 350–600/pack | **ADVANCE** |
| 20 | Menstrual cups 🔴 | Eco-conscious women | — | 1–2 **years** | 1,500–3,000 | Cut — explicitly a durable one-time purchase; fails the core repeat-purchase requirement |
| 21 | Intimate wash | Women | Bottle empties | 6–8 weeks | 400–800 | Keep only as an **upsell** on #19, not standalone (thinner evidence, more sensitive targeting) |
| 22 | Roasted/flavored dry fruit & nut snack boxes 🟢 | Health-conscious snackers, gifting | Eaten and finished | 2–4 weeks | 1,500–4,000 | Keep in Top 10 |
| 23 | Specialty chai / qehwa premix 🟡 (huge macro demand, weak Meta-specific signal — only 13 ads found) | Tea-drinking households (i.e., almost everyone) | Daily staple | 3–5 weeks | 500–1,200 | Keep in Top 10 as a **flagged "test before you trust it" item** |
| 24 | "Verified pure" honey 🟢 (only 2 ads found) | Health-conscious households | Consumed, jar empties | 6–10 weeks | 1,200–3,000 | Cut — very weak Meta signal, heavy glass-jar breakage risk, adulteration-trust problem cuts both ways |
| 25 | Desi masala/spice blend subscription 🔴 | Home cooks | Runs out | 4–8 weeks | 500–1,200 | Cut — no real D2C signal found; National/Shan retail dominance |
| 26 | Protein/energy bars 🔴 | Gym-goers | Eaten, repurchased | 2–4 weeks | 150–300/bar | Cut — insufficient evidence of Pakistani Meta activity; still supplement-adjacent scrutiny |
| 27 | Beard oil / grooming kits 🟢 | Men 18–35 | Daily use, bottle empties | 4–6 weeks | 600–1,500 | Keep in Top 10, flagged — dominated by low-quality generic dropshippers |
| 28 | Razor/blade subscription model 🔴 | Men | Blades dull | 3–4 weeks | 500–1,000 | Cut — no evidence this subscription model exists yet in Pakistan; insufficient evidence |
| 29 | Scented hair mist 🟢 (real: Sanam Jung Fragrances) | Young women | Bottle empties | 6–8 weeks | 500–1,200 | Keep in Top 10 — small but novel, low competition |
| 30 | Baby diapers 🟢 (ad query dominated by noise/spam pages) | Parents of infants | Constant use | 1–2 weeks | 1,500–3,500/pack | Deprioritize — heavy/bulky shipping, thin margin vs. Pampers/Molfix, weak genuine D2C brand signal found |
| 31 | Baby wipes 🟡 | Parents of infants | Constant use | 2–3 weeks | 300–600 | Deprioritize alongside #30 — same competitive dynamic |
| 32 | Multi-surface/dish cleaners 🟢 (near-zero genuine D2C signal) | Households | Bottle empties | 3–5 weeks | 200–500 | **Cut** — Unilever/RB (Vim, Harpic) own 80%+ of this shelf via 258,000 retail points [20][21] |
| 33 | Laundry detergent/pods 🟢 (145 ads, ~100% unrelated noise) | Households | Runs out | 3–4 weeks | 400–900 | **Cut** — no real D2C brand signal; Surf Excel/Ariel/Bonus retail dominance |
| 34 | Whey protein / mass gainer 🟢 (294 real ads — King Nutritions, Styx Nutrition, etc.) | Gym-goers | Tub empties | 4–6 weeks | 2,500–6,000 | **Cut** — real demand, but Meta's Health & Wellness ad policy + your own exclusion criteria on medical/regulatory risk rule it out [29][30] |
| 35 | Contact lens solution | Contact-lens wearers | Bottle empties | 4–8 weeks | 600–1,200 | **Cut** — medical-device-adjacent, small niche, regulatory complexity |

---

## TABLE 2 — FILTERED SHORTLIST (Survivors, With Elimination Logic Applied)

| Product | Shipping Difficulty | COD/RTO Risk | Competition Level | Brand-Building Potential | Upsell/Bundle Potential | Why It Survived |
|---|---|---|---|---|---|---|
| Sunscreen (desi-skin niche) | Low (light plastic tube) | Moderate — liquid product, some leakage-in-transit risk | **High** (2,159 active ads) — real risk of being drowned out | High | High (SPF lip balm, after-sun, moisturizer) | Enormous validated demand; competition is the real risk, needs a sharp wedge |
| Bakhoor/oud home fragrance | Low–moderate (avoid glass/candles in core SKU) | Low — solid consumables, not liquid | **Moderate** (31 active ads) — real but not saturated | Very high — ritual/gifting story | Very high — burner→cones→gift sets→subscription | Best "real demand + real white space" combination found |
| Premium sanitary pads | Low (light, flat packs) | Low-moderate — needs discreet packaging | Moderate — one strong incumbent challenger (Butterfly) already proved the model | High — trust/community brand, proven playbook | High — day/night/maternity/liner range | Best raw repeat-purchase predictability of anything tested (~4 weeks, near-universal) |
| Cat food/litter/treats | **Moderate-high** — litter is heavy, raises per-order courier cost | Moderate | Moderate — Petlife/Meowmarket exist but category still young | High — pet-parent community is a strong brand niche globally | Very high — food+litter+treats+toys naturally basket together | Real, sticky, dedicated sellers found; only concern is thin margin vs. Whiskas price anchor + shipping weight |
| Dry fruits/snack boxes | Moderate (some weight, not fragile) | Moderate | Moderate | Moderate | High (gifting, mix boxes) | Real, active D2C sellers found (Montara, Rayyan Foods, Zouq Foods) |
| Perfume/body-spray bundles | Moderate (glass breakage risk) | Moderate | High (Admiral/RIOS own budget tier) | Moderate | High | Real activity but crowded; treat as secondary line, not lead product |
| Specialty chai/qehwa | Moderate (heavy relative to price) | Moderate | **Low on Meta** (only 13 ads) but that may mean low *convertibility* via COD, not just low competition | High (cultural story) | Moderate | Included as a flagged "test small before betting on it" opportunity — see Red Flags |
| Beard-care kits | Low | Moderate | **High but low-quality** (generic dropshippers dominate) | Moderate | Moderate | Real category, but you'd be fighting price-war dropshippers, not brands |

---

## TABLE 3 — COMPETITOR ANALYSIS

All entries below are **real businesses/pages found via live Meta Ad Library search (queries run 2026-09-19, ads targeting Pakistan) and/or web search** — none invented. Ad Library evidence = the ad was actively running at query time.

### A) Sunscreen / Skincare

| Seller/Store | Product Angle | Price Signal | Marketing Angle | Evidence |
|---|---|---|---|---|
| **Oribelle** | "SPF Is An Everyday Essential," SPF 50 no-greasy-feel | Mid-tier (own store oribellestore.com) | No white cast, lightweight, "Are You Using Enough Sunscreen?" education angle | Live Meta ad + real website + genuine positive reviews (lightweight, no white cast, good for breakout-prone skin) [source: oribellestore.com, live ad query] |
| **De Rien** | "High SPF. Natural-Looking Finish" | Mid-tier | Running a very large number of simultaneous ad variations = serious, sustained spend | Live Meta ad query — highest ad-variant count of any single sunscreen page found |
| **The Skin Scientist** | Generic skincare/derma positioning | Unknown | Multiple active ads, no link-title copy captured | Live Meta ad query |
| **Skindulge** | "Premium Skincare for Radiant, Healthy Skin" | Unknown | Broad-positioning premium skincare | Live Meta ad query |
| **Z&H Collection Hub** | "Get Your Ultimate Glow-Up" | Unknown | General beauty reseller (not sunscreen-specialist) — included for context on general beauty-ad noise | Live Meta ad query |
| Incumbent benchmark: **Hemani, B&B Derma, Eveline, La Roche-Posay, Neutrogena, U-Veil** | Full spectrum budget→premium | Rs. 149 (budget/Hemani) up to premium import tiers | Retail/Daraz shelf presence | Daraz.pk sunscreen blog + pricing pages [8][9] |

**Gap observed:** Almost every ad found leans on generic "SPF/no white cast" messaging. None of the active ads specifically targeted **sweat-resistance for Pakistani summer heat** or **hijab/sport-hijab compatibility** (no smudge under fabric) — a genuine differentiation angle nobody is claiming yet.

### B) Bakhoor / Oud / Home Fragrance

| Seller/Store | Product | Price | Marketing Angle | Evidence |
|---|---|---|---|---|
| **Global-Oud** | Oud/bakhoor sets | Rs. 2,000–3,999 ("limited time" pricing) | Discount urgency, free shipping | Live Meta ad query, multiple repeat campaigns |
| **Hayat Scents** | "Ultimate Bakhoor Starter Set" | Unknown | "Centuries-Old Arab Tradition, Now in Pakistan" — heritage/authenticity angle | Live Meta ad query |
| **Souk Galleria** | "Bakhoor Super Premium Collection" | Unknown | Luxury-deal framing | Live Meta ad query + own site (soukgalleria.com) |
| **Qatada** | Bakhoor/attar | Unknown | "Pakistan's #1 Luxury Brand, Trusted by Legends" | Live Meta ad query |
| **DAR UL MISK** | Attar Bakhoor (Made in KSA), multiple SKUs | Unknown | Imported-authenticity angle (Saudi-sourced) | Live Meta ad query |
| **Natures Bite** | "OUD Mixed Harmal Dhuni" | Unknown | Traditional/spiritual-cleansing angle (harmal/dhuni) | Live Meta ad query |
| **Nirvana Candle Co.** | Scented candles (adjacent category) | Unknown | Discount-driven | Live Meta ad query |
| Incumbent benchmark: **Asgharali** (established Pakistani perfume house) | Bakhoor 80g and oud/bakhoor collection | Established retail pricing | Heritage brand credibility | pk.asgharali.com [source: web search] |

**Gap observed:** Every real player found leans on either "imported/authentic Arabian" or "luxury" framing. Nobody found is positioning bakhoor as an everyday **self-care/ambience ritual for younger, Instagram-native Pakistani buyers** (the way candles or diffusers are marketed in Western markets) rather than a gifting/luxury item — this is the wedge Section "Top 3 Deep Dive" builds on.

### C) Premium Sanitary Pads

| Seller/Store | Product | Price/Positioning | Marketing Angle | Evidence |
|---|---|---|---|---|
| **Butterfly Pakistan** | Full range incl. breathable pads, maternity pads | "Accessible premium" vs. Always | Cottony top-sheet, leak-lock tech, breathability; **documented case study** of winning share from Always via influencer-seeded closed Facebook/Instagram women's groups | Live Meta ad query (many active variants) + own site (butterfly.com.pk) + **75K Instagram followers** [18] + editorial case study in *Profit by Pakistan Today* [19] |
| **LOSHA** | Sanitary pads | Unknown | "Secure From Morning to Night" | Live Meta ad query |
| **Embrace Comfort PK** | Pads | Unknown | "Embrace Womanhood — Best Sanitary Pads for Periods in Pakistan" | Live Meta ad query |
| **Rose Nest** | Pads + bundle sets | AED-denominated (likely cross-border/diaspora reach) | "Ultimate Comfort & Care All in One Value Bundle" | Live Meta ad query |
| Incumbent benchmark: **Always (P&G), Kotex** | Mass retail | Lower price, ubiquitous distribution | Trust via decades of retail presence | Referenced directly in the Butterfly case study [19] |

**Gap observed:** Butterfly's own documented strategy (targeted female micro-influencers, closed groups, breaking taboo through candid content) is public and can be studied — but Butterfly is now the established "modern" option itself. A new entrant needs a distinct sub-angle (e.g., organic-cotton top-sheet, a specific complaint Butterfly reviewers raise, or bundling with heat patches/pain relief) rather than copying its exact playbook.

### D) Cat Food / Litter / Treats

| Seller/Store | Product | Real Price Data | Marketing Angle | Evidence |
|---|---|---|---|---|
| **Petlife.pk (Hospital & Pet Mart)** | Multi-SKU: Bentonite litter, dry/wet food, multiple brands | **Bentonite Cat Litter (Lemon) Rs. 1,330; Mera Cat Food (sensitive stomach) 1.5kg Rs. 3,899; Pick Pure Cat Food 1kg Rs. 880; Pet Nosh PLUS Rs. 10,699; Mito Mix Rs. 22,500; Brit Care Rs. 1,800** | Full-catalog multi-product ad; Lahore-based; self-described "Pakistan's No.1 Online Pet Store" | Live Meta ad query (real SKU-level pricing in ad copy) + petlife.pk site |
| **Meowmarket.pk** | Cat supplies | Unknown | — | Live Meta ad query |
| **Islamabad Enterprises** | "Vet Approved Pawnee" | Unknown | Vet-endorsement angle | Live Meta ad query |
| Incumbent benchmark: **Whiskas (Mars)** | Dry/wet cat food | 800g dry ≈ Rs. 2,060 (was 2,810); 1.9kg dry ≈ Rs. 4,620 (was 6,300) on Daraz | Global brand trust | Daraz.pk pricing pages [16] |
| Also identified (not verified via Ad Library) | PetsMall.pk, Titanspet.pk | — | — | Found via web search only — labeled lower evidence tier |

**Gap observed:** All identified sellers compete on catalog breadth (import resellers). None found are building a **branded, own-formula treats/accessories line** — they're distribution businesses for other brands' food, not a D2C brand with its own product identity. That's the opening.

---

## TABLE 4 — UNIT ECONOMICS

**These figures are a modeled ESTIMATE framework, not measured facts.** Inputs sourced where marked; costs, conversion rates, and RTO-loss assumptions are explicitly labeled. Method: figures are **per delivered order** of a "starter bundle" (defined per product), using Pakistan's sourced COD/RTO/Meta-cost data.

**Sourced inputs used throughout:**
- Courier (forward shipping, light parcel): PKR 150–260 [FACT, courier rate cards, 22]
- COD handling fee: 1.5–2% of order value (retail-tier Leopards rate) [FACT, 23]
- National COD RTO rate: ~18–20% average, 20–35% wider industry range [FACT, 24][25][26]
- Meta cost-per-lead (proxy for cost-per-COD-order-placed) in Pakistan: PKR 281–845 [FACT, 28]
- **CAC per delivered order (ESTIMATE, our calculation)** = (cost-per-order-placed) ÷ (1 − RTO rate) → because ad spend is incurred on every order attempt, whether or not it's ultimately delivered. We use PKR 280/500/850 as low/base/high cost-per-order-placed, giving **CAC ≈ PKR 311 (low) / 625 (base) / 1,214 (high)** per delivered order.
- **RTO waste cost (ESTIMATE, our calculation)** = [RTO rate ÷ (1 − RTO rate)] × (50% of product cost — assuming half is unrecoverable/damaged on return, especially given the common Pakistani COD practice of "open parcel before paying" confirmed directly in one seller's own ad copy — + packaging + forward shipping + an assumed ~PKR 110–150 return-leg courier fee).

| Line Item | Sanitary Pads (3-pack "Starter Bundle," PKR 1,200) | Sunscreen (2-tube bundle, PKR 1,600) | Bakhoor (Starter Ritual Set, PKR 1,800) | Cat Care (New-Parent Box, PKR 1,500) |
|---|---|---|---|---|
| Selling Price | 1,200 | 1,600 | 1,800 | 1,500 |
| − Product Cost (ASSUMPTION) | 220 (base) | 400 (base) | 430 (base) | 700 (base) |
| − Packaging | 35 | 40 | 60 | 45 |
| − Forward Shipping | 200 | 200 | 240 | 300 |
| − COD Fee (~1.5–2%) | 21 | 28 | 32 | 26 |
| − RTO Waste (at 20% base RTO) | 133 | 143 | 161 | 206 |
| − CAC (base) | 625 | 625 | 625 | 625 |
| **= Contribution Profit (BASE)** | **−144** | **+164** | **+252** | **−402** |
| Contribution Profit (LOW: best-case CAC 311, RTO 10%, low costs) | +411 | +763 | +889 | +296 |
| Contribution Profit (HIGH: worst-case CAC 1,214, RTO 30%, high costs) | −1,092 | −836 | −815 | (deeply negative) |
| **Max affordable CAC at BASE (breakeven)** | **~PKR 481** | **~PKR 789** | **~PKR 877** | **~PKR 223** |

### Sensitivity / stress tests (Contribution Profit, PKR, off the BASE case above)

| Product | BASE | CAC +25% | CAC +50% | RTO → 10% | RTO → 30% | Product Cost +15% |
|---|---|---|---|---|---|---|
| Sanitary Pads | −144 | −300 | −457 | −70 | −305 | −194 |
| Sunscreen | +164 | +8 | −149 | +260 | −13 | +104 |
| Bakhoor | +252 | +96 | −61 | +360 | +48 | ~+187 |
| Cat Care | −402 | −558 | −715 | −266 | −653 | −507 |

**What this actually says:** at Pakistan's real, sourced ~20% national RTO average and a realistic Meta-derived CAC, **first-order economics are negative-to-thin for three of the four candidates, and only genuinely positive for Bakhoor.** This is not a reason to give up — it is why Step 6 (repeat-purchase economics) below matters more than first-order profit. It does mean: (a) you must fight to keep CAC toward the low end (strong creative, not just "boost post"), (b) you must actively suppress RTO below the national average via order-confirmation calls (a standard practice among Pakistani COD operators), and (c) **Cat Care's staple-food/litter bundle should not be your acquisition offer** — its margin is too thin to absorb realistic CAC; treasts/accessories (higher markup) should be the acquisition hook, with food/litter reserved for the repeat/subscription stage once trust and delivery-cost efficiency (larger, less-frequent orders) are established.

---

## TABLE 5 — REPEAT PURCHASE ECONOMICS

**A) First-Order Economics** (from Table 4, BASE case)

| Product | First Order Value | First-Order Contribution (BASE) |
|---|---|---|
| Sanitary Pads | 1,200 | −144 |
| Sunscreen | 1,600 | +164 |
| Bakhoor | 1,800 | +252 |
| Cat Care | 1,500 | −402 |

**B) Repeat-Order Economics** — ASSUMPTION: repeat RTO drops to ~7% (established trust, known address, self-selected satisfied buyer) and CAC collapses to a small retention-messaging cost (~PKR 10/order via WhatsApp/SMS reminders) rather than paid Meta CAC.

| Product | Repeat Order Contribution (ESTIMATE) | Repurchase Interval (ASSUMPTION) | Purchases/Year (ASSUMPTION) | 12-Month Revenue/Customer | **12-Month Gross Profit/Customer (LTV, ESTIMATE)** |
|---|---|---|---|---|---|
| Sanitary Pads | +564 | ~5–6 weeks | ~9 | ~10,800 | **~4,368** |
| Sunscreen | +879 | ~10 weeks | ~5 | ~8,000 | **~3,680** |
| Bakhoor | +980 | ~6 weeks (lumpy: Ramadan/Eid/wedding-season spikes) | ~8 | ~14,400 | **~7,112** |
| Cat Care | +357 | ~4 weeks (most frequent of the four) | ~12 | ~18,000 | **~3,525** |

**The core finding:** every one of these businesses is a **repeat-purchase business or it is not a business at all.** Bakhoor produces the best 12-month gross profit per customer despite the smallest total market, because its margin structure absorbs CAC/RTO shocks best. Cat Care has the highest raw purchase *frequency* but the thinnest per-order margin, so it converts frequency into profit the least efficiently of the four — unless the SKU mix is redesigned around higher-margin items.

**Reducing Meta dependency over time:** all four categories support a realistic shift away from paid acquisition once you have ~500–1,000 customers:
- **WhatsApp** — Pakistan's dominant messaging channel; a simple broadcast list or WhatsApp Business catalog for reorder reminders costs near-zero marginal spend and is explicitly called out as the highest-converting channel for Pakistani D2C brands in industry guides [6].
- **SMS** — cheap, high open-rate reorder nudges timed to the repurchase interval (e.g., day 25 of a 28-day pad cycle).
- **Instagram/Facebook retargeting** — retargeting past purchasers is dramatically cheaper CPM than cold prospecting.
- **Reorder reminders tied to the interval itself** — this is the one lever unique to consumable products (a gadget seller has nothing equivalent): you know almost exactly when a sunscreen tube runs out, so you can message *before* the customer even feels the need, pre-empting a competitor's ad.

---

## TABLE 6 — TOP 10 OPPORTUNITIES (Evidence-Weighted Scoring Matrix)

Weights per your framework: Demand 20% · Repeat Potential 20% · Meta Ads Potential 15% · Gross Margin 15% · Competition Opportunity 10% · Shipping/COD Practicality 10% · Brand-Building 5% · Upsell/Bundle 5%. **Scores are a research framework to compare relative evidence strength, not a guarantee of outcomes.**

| Rank | Product | Demand (20%) | Repeat (20%) | Meta Ads (15%) | Margin (15%) | Competition Opp. (10%) | Shipping/COD (10%) | Brand (5%) | Upsell (5%) | **Weighted Score** |
|---|---|---|---|---|---|---|---|---|---|---|
| 1 | **Premium Sanitary Pads** | 9 | 10 | 6 | 6 | 5 | 8 | 8 | 8 | **7.70** |
| 2 | **Sunscreen (desi-skin)** | 9 | 8 | 8 | 6 | 4 | 8 | 7 | 7 | **7.40** |
| 3 | **Bakhoor/Home Fragrance** | 6 | 7 | 7 | 8 | 7 | 7 | 9 | 9 | **7.15** |
| 4 | **Cat Food/Litter/Treats** | 6 | 9 | 8 | 6 | 6 | 5 | 8 | 9 | **7.05** |
| 5 | Specialty Chai/Qehwa | 8 | 8 | 3 | 5 | 7 | 5 | 7 | 6 | 6.25 |
| 6 | Dry Fruits/Snack Boxes | 7 | 6 | 6 | 5 | 5 | 7 | 6 | 7 | 6.10 |
| 7 | Scented Hair Mist | 4 | 6 | 6 | 7 | 7 | 7 | 6 | 5 | 5.90 |
| 8 | Perfume/Body Spray Bundles | 6 | 6 | 6 | 6 | 4 | 6 | 6 | 7 | 5.85 |
| 9 | Soy/Scented Candles | 5 | 6 | 6 | 7 | 6 | 3 | 7 | 6 | 5.70 |
| 10 | Beard-Care Kits | 5 | 6 | 5 | 6 | 3 | 7 | 5 | 6 | 5.40 |

**Evidence behind the top-4 scores (the ones that matter most):**
- *Sanitary Pads* scores highest almost entirely on **Repeat (10/10)** — a ~4-week, near-universal, non-discretionary cycle is the most predictable of anything researched — and solid Brand/Upsell scores backed by Butterfly's real case study. Its weak points are margin and competition (an entrenched local challenger already exists).
- *Sunscreen* scores highest on raw **Demand (9/10)** — 2,159 live ads is the single largest signal found in this entire research process — but Competition Opportunity is the lowest of the top 4 (4/10): you are entering the most crowded pool.
- *Bakhoor* is the only one of the four with a genuinely high **Competition Opportunity (7/10)** score — real demand, but not yet fought over — plus the best margin and brand-building scores of any candidate.
- *Cat Care* scores highest on **Meta Ads potential (8/10)** — pet content is inherently algorithm- and UGC-friendly — but the lowest Shipping/COD score (5/10) of the top 4 due to litter's weight.

---

## TOP 3 DEEP DIVE

### 1. Premium Breathable Sanitary Pads

1. **Exact niche:** Mid-premium, breathable-top-sheet sanitary pads sold direct-to-consumer, positioned between mass-market retail packs and imported premium brands.
2. **Ideal customer:** Women 16–40 in urban/peri-urban Pakistan with smartphone + Meta access, currently buying pads at a local pharmacy/kiryana store out of habit rather than preference.
3. **Core problem:** Discomfort, leakage anxiety, and rash/heat irritation from cheaper mass-market pads in Pakistan's climate; also the discretion/embarrassment of buying in person.
4. **Why they buy:** Comfort/breathability claims are easy to believe and cheap to trial (low price point, low risk); discreet home delivery removes a real social-friction point Butterfly's own marketing explicitly leaned on [19].
5. **Why they reorder:** It's not optional — non-discretionary, biologically scheduled demand, the single most predictable repeat mechanic in this entire report.
6. **Expected reorder interval:** ~4–6 weeks (ASSUMPTION, tied to menstrual cycle + pack size).
7. **Suggested price range:** PKR 350–600 per pack retail; PKR 1,200–1,500 for a 3-pack "starter" bundle.
8. **Target gross margin:** 60–75% before CAC/RTO/shipping (i.e., product+packaging cost around 25–35% of price) — ASSUMPTION based on typical FMCG hygiene cost ratios.
9. **Estimated CAC ceiling:** ~PKR 480 per delivered order at base bundle price (Table 4) — meaningfully below the sourced PKR 625 base CAC estimate, meaning **you need to beat average Meta performance, not just meet it**, or raise the bundle size.
10. **Competitors:** Butterfly Pakistan (dominant local challenger, 75K IG followers), LOSHA, Embrace Comfort PK, Rose Nest; incumbents Always (P&G), Kotex.
11. **Competitor pricing:** Butterfly positions as "accessible premium" below Always; exact PKR price points not published in the sources found — **insufficient evidence** for exact competitor SKU pricing; treat as a real gap to fill with your own mystery-shopping before finalizing price.
12. **Differentiation strategy:** Don't copy Butterfly's now-established "modern brand" positioning — instead pick a specific, provable sub-claim (e.g., organic cotton top-sheet, dermatologically tested for sensitive skin, or a bundled heat-patch/pain-relief add-on that Butterfly does not offer) and back it with real certification, not just marketing copy.
13. **Bundle strategy:** Trial Duo (2 packs) → Starter Bundle (3 packs + travel pouch) → Monthly Value Pack (day + night + liners) → Family/Multi-user pack.
14. **Repeat-order strategy:** Pre-emptive WhatsApp reorder reminder timed to day ~24–26 of the average cycle; loyalty discount on 3rd order; subscribe-and-save option once trust is established.
15. **Meta Ads creative strategy:** UGC-style testimonials from real (paid, disclosed) users on comfort/breathability; avoid explicit personal-health targeting (Meta restricts inferring menstrual status) — use broad/interest targeting (women's lifestyle, beauty, wellness interests) exactly as Butterfly's documented playbook did via seeded closed groups [19] rather than direct demographic-health targeting.
16. **Landing/product page structure:** Above the fold = comfort/breathability claim + discreet-packaging reassurance + price; middle = certification/material callouts + real reviews; bottom = bundle options + COD/discreet-delivery FAQ.
17. **WhatsApp reorder strategy:** Order confirmation → delivery confirmation → day-24 reorder nudge with one-tap reorder link → post-purchase satisfaction check.
18. **Main risks:** Thin first-order margin (Table 4 shows negative BASE contribution); an entrenched, well-loved local challenger already occupies the "modern brand" position; COD cash handoff for a period product can carry mild social friction with a male rider in conservative households — discreet packaging is not optional, it's core product design.
19. **Regulatory/advertising risks:** Meta restricts ads from asserting/inferring personal health attributes — creative must stay in lifestyle/comfort language, not clinical claims. **Insufficient evidence found on exact DRAP (Drug Regulatory Authority of Pakistan) classification for sanitary pads** — confirm with a local regulatory consultant before launch rather than assuming.
20. **Sourcing difficulty:** Moderate — requires either a local contract manufacturer willing to private-label (Pakistan has an existing hygiene-manufacturing base given Butterfly's own local success) or importing; MOQs for private-label hygiene products are typically non-trivial (thousands of packs) — this is the most capital-intensive of the three finalists to source properly.
21. **Minimum viable launch plan:** Start by reselling/private-labeling a single SKU (one absorbency level) rather than a full range; validate creative and CAC with a small batch before committing to a larger MOQ.
22. **What to test first:** Whether a specific, provable differentiation claim (not just "premium") can pull CAC below the PKR 480 ceiling — test 3–4 distinct claim-led creatives before spending on production scale-up.

### 2. Lightweight, No-White-Cast Sunscreen (Desi-Skin Niche)

1. **Exact niche:** Cosmetic sunscreen specifically engineered/marketed against the "white cast, greasy feel" complaint that dominates real reviews of existing options for South Asian skin tones.
2. **Ideal customer:** Urban women 18–35, skincare-engaged (follows beauty content), currently either not using sunscreen consistently or unhappy with what they use.
3. **Core problem:** Most sunscreen formulas leave a visible white/grey cast on medium-to-deep skin tones and feel heavy/sticky in Pakistan's heat and humidity.
4. **Why they buy:** The "no white cast" claim is instantly, visually demonstrable in a 5-second video — this is one of the single most share-tested content formats in global beauty marketing, applied to a local skin-tone need.
5. **Why they reorder:** Daily-use consumable; once a customer finds a formula that genuinely doesn't cast, switching cost (re-testing an unknown brand) is high, which helps retention.
6. **Expected reorder interval:** ~4–8 weeks depending on application habits (ASSUMPTION, standard dermatological usage-rate estimate).
7. **Suggested price range:** PKR 800–1,600 per 50ml tube; PKR 1,600 for a 2-tube bundle.
8. **Target gross margin:** 65–75% before CAC/RTO — ASSUMPTION.
9. **Estimated CAC ceiling:** ~PKR 789 per delivered order at base bundle price (Table 4) — the healthiest CAC cushion of the three finalists, because the higher AOV absorbs cost better.
10. **Competitors:** Oribelle, De Rien (heaviest ad spend observed), The Skin Scientist, Skindulge; incumbent retail brands Hemani (budget), La Roche-Posay (premium import).
11. **Competitor pricing:** Daraz-wide sunscreen prices start at Rs. 149 (budget/local) up through premium imports [9]; Oribelle/De Rien sit in an inferred mid-premium band based on ad positioning, exact price not confirmed in sources found — **insufficient evidence** for their precise PKR price; verify directly before setting your own price.
12. **Differentiation strategy:** Every active ad found leans on generic "no white cast/lightweight" language. None claims **sweat/humidity resistance for outdoor work commutes** or **compatibility under makeup/hijab without pilling** — pick one specific, testable claim and prove it on camera rather than repeating the same message as De Rien.
13. **Bundle strategy:** Single trial tube → 2-tube bundle (recommended entry, better AOV/CAC ratio) → Daily Ritual Set (sunscreen + lip SPF) → Family/skin-type range → Subscription refill.
14. **Repeat-order strategy:** Usage-based reminder (tube typically empties in ~5–6 weeks) via WhatsApp; loyalty pricing on subscription refill.
15. **Meta Ads creative strategy:** Direct-to-camera "apply and blend" demonstration under different lighting to prove no-cast claim; UGC creator partnerships are straightforward here since the product is inherently visual and safe (no medical claim needed — this is a cosmetic finish claim, not a health claim).
16. **Landing/product page structure:** Above fold = the no-white-cast demo (video/GIF) + price; middle = ingredient/SPF-test certification (see risk below) + skin-tone-inclusive before/after; bottom = bundle CTA + reviews.
17. **WhatsApp reorder strategy:** Tube-life-based reminder (~day 35–40) with a direct reorder link; seasonal push before summer.
18. **Main risks:** The single most crowded category researched (2,159 active competing ads) — real risk of high CPMs and being outspent by De Rien; HIGH stress-case CAC wipes out margin entirely (Table 4 sensitivity: −836 at high CAC/RTO).
19. **Regulatory/advertising risks:** SPF numbers are a testable, falsifiable claim — **do not state an SPF number without a real lab test certificate from your manufacturer.** This is a genuine legal/reputational exposure if a supplier's claimed SPF isn't real, distinct from a "medical claim" but just as damaging if wrong.
20. **Sourcing difficulty:** Moderate — cosmetic private-label manufacturers (regionally, often via Chinese/Korean or Pakistani contract cosmetic labs) commonly offer sunscreen at workable MOQs; the harder part is verifying real SPF test documentation, not finding a factory.
21. **Minimum viable launch plan:** Launch with one hero SKU and one sharp claim; do not attempt a "full skincare line" out of the gate.
22. **What to test first:** Whether your specific differentiation angle (sweat-resistance, hijab-compatibility, or similar) actually produces a lower CPC/CVR than a generic "no white cast" ad before scaling spend — you're testing whether you can beat the crowd, not whether the category works (it clearly does).

### 3. Bakhoor / Oud / Attar Home-Fragrance Ritual Kits

1. **Exact niche:** Modern, ritual/self-care-framed bakhoor and attar starter kits (burner + cones/resin + attar sample), targeting younger urban buyers rather than the "luxury Arabian import" framing every current competitor uses.
2. **Ideal customer:** Urban women and men 20–40 who already spend on home decor/self-care content on Instagram, plus gifting occasions (Eid, weddings, housewarmings).
3. **Core problem:** Existing bakhoor options are framed as either expensive imported luxury or traditional/religious-only use — nobody is selling it as an everyday ambience/self-care ritual the way candles or diffusers are marketed elsewhere.
4. **Why they buy:** Sensory, aesthetic, and cultural resonance; low first-purchase risk given moderate price points found in the market (Rs. 400–4,000 range depending on tier).
5. **Why they reorder:** Cones/resin/attar are physically consumed with use — this is a genuinely consumable ritual product, not a durable good.
6. **Expected reorder interval:** ~4–6 weeks for regular users, though genuinely lumpy around Ramadan, Eid, and wedding season (ASSUMPTION, consistent with cultural usage patterns).
7. **Suggested price range:** PKR 1,200–2,500 for a starter ritual set; PKR 400–800 for cone/resin refill packs.
8. **Target gross margin:** 70–80% before CAC/RTO — the best of the three finalists, since raw bakhoor/resin material cost is low relative to perceived value (ASSUMPTION, consistent with fragrance/home-decor category norms generally).
9. **Estimated CAC ceiling:** ~PKR 877 per delivered order at base set price (Table 4) — the highest (most forgiving) ceiling of the three finalists.
10. **Competitors:** Global-Oud, Hayat Scents, Vibe Fragrances, Qatada, Souk Galleria, DAR UL MISK, Natures Bite; incumbent Asgharali (established perfume house with its own bakhoor line).
11. **Competitor pricing:** Global-Oud advertised Rs. 2,000 and Rs. 3,999 price points (limited-time framing, so likely list price is somewhat higher); other real prices not confirmed in sources found — **insufficient evidence** on Hayat Scents/Souk Galleria exact pricing; mystery-shop before finalizing your own.
12. **Differentiation strategy:** Reframe from "luxury Arabian import" to "everyday ritual for your home" — modern minimalist packaging, lifestyle content (working from home, self-care evenings) rather than the wedding/luxury-gifting-only framing every competitor found uses.
13. **Bundle strategy:** Trial cone pack → Starter Ritual Set (burner + cones + attar sample) → Seasonal Gift Set (Ramadan/Eid) → Refill Subscription (cones/resin only, once burner is owned).
14. **Repeat-order strategy:** Because the burner is a durable component and only cones/resin are consumed, the repeat SKU is naturally cheaper and higher-margin than the entry SKU — ideal for a refill subscription pitched directly on WhatsApp.
15. **Meta Ads creative strategy:** Purely sensory/aesthetic video (smoke, ambience, unboxing) — the easiest of the three finalists to produce cheaply and authentically without needing dermatologist-style proof or clinical claims.
16. **Landing/product page structure:** Above fold = aesthetic ritual video + starter set price; middle = "what's inside" breakdown + safety/usage instructions; bottom = gifting angle + subscription refill CTA.
17. **WhatsApp reorder strategy:** Refill reminder timed to typical cone-pack usage (~5 weeks) + seasonal push ahead of Ramadan/Eid.
18. **Main risks:** Smaller total addressable market than sunscreen or pads; demand is genuinely seasonal/lumpy (Ramadan/Eid/wedding season spikes), which complicates steady-state ad budgeting; candle line extensions carry real melt/breakage risk in Pakistani summer transit — keep candles as a cautious add-on, not the core SKU.
19. **Regulatory/advertising risks:** Lowest of the three finalists — no medical, cosmetic-claim, or personal-health-adjacent issues. The one real operational risk is **fire/burn safety** (charcoal/cone burning indoors) — include clear safety instructions and consider this a product-liability, not ad-policy, consideration.
20. **Sourcing difficulty:** Lowest of the three finalists — bakhoor, resin, and attar are sourced from existing Pakistani wholesale fragrance markets (e.g., established fragrance/attar wholesale trade in Lahore/Karachi); simple metal/ceramic burners are a standard, low-MOQ sourced item.
21. **Minimum viable launch plan:** Source a small batch (a few hundred units) of one starter-set configuration from an existing wholesale attar/bakhoor supplier before committing to custom packaging or private formulation.
22. **What to test first:** Whether "everyday ritual" framing outperforms the "luxury/imported" framing every competitor currently uses — this is a genuinely testable creative hypothesis with a clear, cheap way to measure it (CTR/CVR on two creative sets).

---

## META ADS TESTING PLAN

*(Condensed for the two highest-conviction starting points — Bakhoor for lowest-capital entry, Sanitary Pads for highest long-run conviction. Apply the same framework to Sunscreen once you have a validated differentiation angle.)*

### Bakhoor / Home-Fragrance Ritual Kits

- **5 ad angles:** (1) "Your home deserves a ritual, not just a scent" (everyday self-care reframe) (2) Heritage/authenticity ("sourced from Pakistan's oldest attar markets") (3) Gifting ("the Eidi they'll actually love") (4) Sensory ASMR (smoke/sound/aesthetic, minimal text) (5) Problem-agitation ("your home smells like nothing — here's why that's a missed ritual")
- **5 hooks (first line/first 3 seconds):** (1) Close-up shot of smoke curling from a lit cone, silence, then reveal (2) "This is why guests always ask what that smell is" (3) "I used to only light this for guests. Now it's every evening." (4) Unboxing reveal of the starter set (5) Split-screen: cluttered/plain room vs. same room with bakhoor ambience
- **3 UGC concepts:** (1) "My evening wind-down ritual" day-in-the-life creator video (2) Real customer unboxing + first reaction (3) "Things I didn't know I needed for my home" multi-product roundup featuring the starter set
- **3 demonstration concepts:** (1) Lighting a cone start-to-finish in real time with ambient sound (2) Side-by-side of different scents with visible smoke density (3) "What's in the box" flat-lay breakdown
- **3 offer ideas:** (1) Starter Ritual Set at a launch price with free second scent (2) Buy-2-cone-packs-get-1-free (3) Free burner with first attar purchase above a threshold
- **Target audience hypotheses:** Broad Pakistan 20–45 interested in home decor/lifestyle content; a secondary narrower set interested in Islamic lifestyle/Ramadan content for seasonal pushes
- **Broad vs. interest targeting:** Start broad (Meta's algorithm targeting) given the small dataset needed to find buyers in a niche category — narrow interest targeting on "oud"/"perfume" risks being too small and expensive; use interest layers only for seasonal (Ramadan/Eid) campaigns
- **Initial testing budget:** PKR 30,000–50,000 over 2 weeks (small-capital realistic starting point)
- **Number of creatives to test:** 6–8 initial creative variants across the 5 angles above, rotated in pairs
- **Kill criteria:** Any ad with CPC > ~2x account average after PKR 3,000 spend with zero orders; any angle producing no "Initiate Checkout" events after PKR 5,000
- **Scaling criteria:** Once one angle produces a delivered-order CAC at or below the ~PKR 877 ceiling (Table 4) consistently over 20+ orders, increase budget 20–30% every 3–4 days rather than doubling abruptly

### Premium Sanitary Pads

- **5 ad angles:** (1) Comfort/breathability demonstration (2) Discreet delivery reassurance (3) "Why I switched" testimonial (4) Certification/material credibility (5) Bundle value framing
- **5 hooks:** (1) "Nobody talks about this, but I will" (taboo-breaking opener) (2) Close-up fabric/texture shot with voiceover on breathability (3) "POV: you found a pad that doesn't feel like plastic" (4) Real customer testimonial cold open (5) Discreet-packaging reveal ("this is what arrives at your door")
- **3 UGC concepts:** (1) Real (compensated, disclosed) customer testimonial on comfort (2) "What's in my bag" style content naturally featuring the product (3) Closed-group-seeded testimonial content, following Butterfly's documented approach [19]
- **3 demonstration concepts:** (1) Absorbency/breathability material demo (non-graphic, texture-focused) (2) Discreet packaging unboxing (3) Size/range comparison (day vs. night vs. liner)
- **3 offer ideas:** (1) Trial Duo at a low entry price (2) Starter Bundle with free travel pouch (3) Subscribe-and-save on the 2nd order
- **Target audience hypotheses:** Broad women 18–40 Pakistan-wide; lifestyle/beauty/wellness interest layers rather than any health-status inference (Meta policy risk)
- **Broad vs. interest targeting:** Broad targeting recommended as primary, consistent with Meta's own Advantage+ guidance and the fact that health-status inference targeting is restricted; interest layers on general beauty/lifestyle as a secondary test
- **Initial testing budget:** PKR 40,000–60,000 over 2–3 weeks (slightly higher than Bakhoor given higher MOQ/sourcing cost already sunk)
- **Number of creatives to test:** 6–8 variants, prioritizing UGC/testimonial formats given the trust-building nature of the category
- **Kill criteria:** Same framework as above; specifically watch for ad rejections (Meta may flag health-adjacent creative) and be ready to revise copy toward lifestyle language
- **Scaling criteria:** Scale only once delivered-order CAC is demonstrably below the PKR 481 breakeven ceiling — this category's tighter margin means scaling too early on hope, not data, is the most likely failure mode

---

## 90-DAY LAUNCH STRATEGY

**Recommended sequencing:** Given "relatively small starting capital," lead with **Bakhoor** — lowest MOQ, lowest regulatory complexity, best margin cushion against the CAC/RTO shocks Table 4 shows are real. Treat Sanitary Pads as the priority second product once you have working capital and a proven RTO-control process (confirmation calls, verified addresses). Only enter Sunscreen once you have a genuinely tested, provable differentiation claim — entering that category without one means competing directly against De Rien's ad budget.

**Days 1–15 — Setup & Sourcing**
- Register business basics (bank account capable of receiving COD settlements from your courier partner)
- Identify and sample from 2–3 wholesale bakhoor/attar suppliers; select one starter-set configuration
- Set up a simple landing page (Shopify or a local COD-store builder) with WhatsApp Business catalog
- Open a Leopards/TCS retail or small-business courier account; confirm COD settlement terms
- Set up Meta Business Manager, Page, and Pixel/Conversions API

**Days 16–30 — Creative & Small-Batch Test**
- Produce 6–8 creatives per the testing plan above using your own phone (no need for expensive production for the sensory/ritual angle)
- Run PKR 30,000–50,000 in initial spend across the 5 angles
- Manually call every order to confirm before dispatch (this single step is the highest-leverage RTO-reduction tactic available to a small operator)
- Track actual CAC and RTO against the Table 4 model — replace every ASSUMPTION in this report with your own real number as soon as you have 30+ orders

**Days 31–60 — Iterate**
- Kill underperforming angles per the kill criteria; double down on the winning hook/angle
- Introduce the refill/subscription SKU to your first 30–50 customers via WhatsApp — this is your first real repeat-purchase data point
- Begin sourcing conversations for the second product (Sanitary Pads) in parallel, but do not launch it until Bakhoor's CAC and RTO are under control

**Days 61–90 — Scale & Layer**
- Scale winning Bakhoor creative per scaling criteria
- Launch Sanitary Pads as a second, separate campaign once sourcing is confirmed — do not run it from the same Page/Pixel budget as Bakhoor without separating budgets, since their unit economics are very different
- Build your first WhatsApp broadcast list from Bakhoor customers and send the first reorder reminder campaign to measure real (not modeled) repeat-order economics

**What to test first, across everything:** whether your actual CAC and RTO land near this report's LOW scenario or its HIGH scenario. That single answer — not the product choice itself — determines whether any of these businesses works.

---

## RISKS & RED FLAGS

**Brutally, without motivational language:**

### Sanitary Pads
- **What could make this fail:** First-order economics are modeled negative at base assumptions (Table 4: −144). If your real CAC lands anywhere near the sourced PKR 625 base-case Meta cost, and your RTO sits at Pakistan's documented national average (18–20%), **you lose money on every first order** and the business only works if repeat-purchase rates and retention (via WhatsApp) are executed well — this is an execution-dependent business, not a "list it and it sells" business. A well-funded, already-trusted local incumbent (Butterfly) occupies the exact positioning a new entrant would naturally reach for.
- If you cannot get CAC under ~PKR 480 or push RTO below ~15%, **the economics do not work as modeled** — say so honestly rather than assuming marketing will fix it.

### Sunscreen
- **What could make this fail:** This is the most crowded category in this entire report (2,159 active competing ads). De Rien alone is running enough ad variants to suggest a well-funded, sophisticated competitor already iterating fast. A small new entrant without a genuinely differentiated, *provable* claim will likely see CPMs pushed up by this competition and get outspent rather than outmaneuvered. High-stress-case contribution is deeply negative (−836).
- Claiming an SPF number you have not had independently tested is a real legal/reputational risk, separate from Meta ad policy — this is not a "medical claim" grey area, it's a straightforward false-advertising exposure if wrong.

### Bakhoor
- **What could make this fail:** This is a genuinely smaller total market than the other three — the "least saturated" finding cuts both ways; it may be under-fought-over *because* Pakistani consumers don't yet buy it this way via COD/Meta ads at scale, not only because nobody has tried. Demand is seasonally lumpy (Ramadan/Eid/wedding season), which makes steady-state customer acquisition harder to plan around than a daily-use consumable. If candle line-extensions are added carelessly, Pakistan's summer transit heat creates real melt/breakage/refund exposure that could quietly erode margin without showing up until refund requests spike.
- **Insufficient evidence** exists in this research to state confidently how large the addressable online-buying market for this category actually is beyond the ~31 active-ad signal — treat the 90-day test as a genuine validation exercise, not a foregone conclusion.

### Cat Care (why it did not make the Top 3 despite strong qualitative appeal)
- The modeled economics are the worst of the four candidates researched (Table 4: −402 base contribution, and stress scenarios push it to −650 to −715). Litter's weight inflates courier cost, and Whiskas' real, publicly visible Daraz pricing (Rs. 2,060–4,620) puts a hard ceiling on how much you can charge for food without losing on direct price comparison. **If your acquisition offer is a food/litter-anchored bundle, the numbers in this report say it does not work** at realistic CAC — only a treats/accessories-led acquisition strategy, with food/litter reserved for retained repeat customers, has a plausible path to profitability. This is exactly the kind of case the brief asked to flag rather than paper over.

### Across all four
- **Every single unit-economics figure in Table 4/5 is a modeled ESTIMATE**, built transparently from sourced inputs (courier rates, national RTO average, Meta cost-per-lead benchmarks) but not measured from an actual Pakistani operator's books. Treat the LOW/BASE/HIGH range as the honest range of outcomes, not the BASE case as a promise.
- I could not verify: exact competitor unit sales, exact competitor revenue, exact real-world CAC for any of these specific sellers, or exact search-volume/Google-Trends data (tool limitation, stated up front). Anywhere this report states a number, it is FACT (sourced), ESTIMATE (modeled, shown), or ASSUMPTION (labeled) — never fabricated.
- Pakistan's COD RTO reality (18–35% depending on source) is worse than many first-time founders assume before they see real numbers — budget and cash-flow planning should use the higher end of this range until your own data says otherwise.

---

## SOURCES

| # | Website | Page/Article | URL | Claim It Supports |
|---|---|---|---|---|
| 1 | Yahoo Finance / Report reprint | Pakistan B2C Ecommerce Report 2025 | https://finance.yahoo.com/news/pakistan-b2c-ecommerce-report-2025-111100909.html | Market size ~$14.11B by 2025 → $20.41B by 2029, 13.2% growth, fashion 28%/electronics 24% share |
| 2 | ecdb.com | E-Commerce in Pakistan: Market Size, Platforms & Statistics | https://ecdb.com/resources/sample-data/market/pk/all | General market size/platform data |
| 3 | PaymentsCMI | E-commerce Projections for Pakistan (2024–2027) | https://paymentscmi.com/insights/pakistan-ecommerce-market-data/ | Market projections |
| 4 | Accio | Top Selling Products on Daraz Pakistan 2026 | https://www.accio.com/business/top-selling-products-on-daraz-pakistan | Grocery/beauty as fastest-growing categories |
| 5 | Accio | Daraz Best Selling Products | https://www.accio.com/business/daraz-best-selling-products | Facial masks/skincare sets = highest sales velocity on Daraz |
| 6 | Unboxed Global | Facebook, Instagram & TikTok Ads Cost in Pakistan 2026 | https://unboxed.global/social-media-ads-cost-pakistan/ | Pakistan Meta ad cost/behavior context |
| 7 | Madiha Digital | Meta Ads Pakistan 2026 Guide | https://www.madihadigital.online/blog/meta-ads-pakistan-guide | COD-dominant market needs brand trust before conversion; WhatsApp/Reels behavior |
| 8 | Daraz Blog | 10 Best Sunscreen Brands Available in Pakistan | https://blog.daraz.pk/best-sunscreen-in-pakistan-with-price/ | Sunscreen brand landscape in Pakistan |
| 9 | Pakistanistores.com | Sunscreen Price in Pakistan | https://pakistanistores.com/prices/beauty--health/beauty/face/sunscreen | Sunscreen prices start from Rs. 149 |
| 10 | Oribelle | Oribelle Store | https://oribellestore.com/ | Brand positioning, reviews (no white cast, lightweight) |
| 11 | Souk Galleria | Bakhoor Super Premium Collection | https://www.soukgalleria.com/collections/bakhoor-super-premium-collection | Real bakhoor D2C seller evidence |
| 12 | Asgharali Pakistan | Oudh & Bakhoor Collection | https://pk.asgharali.com/collections/oudh-bakhoor | Incumbent Pakistani perfume house's bakhoor line |
| 13 | Motiza.pk | Bakhoor Collection | https://motiza.pk/collections/bakhoor | Additional real bakhoor D2C evidence |
| 14 | Petlife.pk | Petlife – Pakistan's No.1 Online Pet Store | https://petlife.pk/ | Real pet-store business, product catalog |
| 15 | Dogster | 15 Pakistan Pet Industry Statistics 2026 | https://www.dogster.com/statistics/pakistan-pet-industry-statistics/ | Pet population growth claim (flagged as lower-confidence source) |
| 16 | Daraz.pk | Whiskas Products Price List in Pakistan | https://www.daraz.pk/whiskas/ | Whiskas real pricing (Rs. 2,060 / Rs. 4,620) |
| 17 | Butterfly Pakistan | Official site | https://butterfly.com.pk/ | Brand/product information |
| 18 | Instagram | @butterflypakistanofficial | https://www.instagram.com/butterflypakistanofficial/?hl=en | 75K follower count |
| 19 | Profit by Pakistan Today | How Butterfly is beating back Always in the sanitary napkins market | https://profit.pakistantoday.com.pk/2021/04/25/how-butterfly-is-beating-back-always-in-the-sanitary-napkins-market/ | Case study: challenger brand strategy vs. Always |
| 20 | Unilever | Inside our markets: Unilever's business in Pakistan | https://www.unilever.com/news/news-search/2023/inside-our-markets-unilevers-business-in-pakistan/ | 258,000-store distribution network — basis for eliminating household cleaning |
| 21 | Aurora (Dawn) | Domex – another germ buster? | https://aurora.dawn.com/news/1141890/domex-another-germ-buster | Harpic 80%+ share of branded toilet-cleaner segment |
| 22 | TrackMyOrder.pk | Pakistan Courier Rates 2026 — TCS, Leopards & M&P | https://trackmyorder.pk/blog/comparisons/pakistan-courier-rates-2026-tcs-leopards-mnp | Courier rate cards |
| 23 | TrackMyOrder.pk | Leopards Courier Rates 2026 | https://trackmyorder.pk/blog/guides/leopards-courier-rates-2026 | COD fee 1.5–2% retail / 0.75–1.5% corporate |
| 24 | TrackMyOrder.pk | COD Return Rate in Pakistan: What's Normal | https://trackmyorder.pk/blog/shopify-tips/cod-return-rate-pakistan-shopify | National RTO average 18–20% |
| 25 | OrderNation | State of Online Shopping in Pakistan 2026 | https://www.ordernation.com/blogs/research/state-of-online-shopping-pakistan-2026 | COD = 80%+ of transactions; RTO context |
| 26 | eGrow | The Complete Guide to Reducing RTO in COD E-commerce (2026) | https://www.egrow.com/en/blog/the-complete-guide-to-reducing-return-to-origin-rto-in-cod-e-commerce-2026 | RTO industry range 20–35% |
| 27 | EasySellApp | COD Ecommerce Pakistan & Bangladesh | https://easysellapp.com/blogs/wiki/cod-ecommerce-pakistan-bangladesh-cash-collection-delivery-2026 | COD conversion-funnel context |
| 28 | Siffar | Facebook Ads Cost in Pakistan 2026 | https://siffar.com/facebook-ads-costs-in-pakistan-a-comprehensive-guide-for-2025/ | Meta CPC PKR 140–422 (traffic), PKR 281–845 (lead) |
| 29 | Meta Transparency Center | Health and Wellness — Restricted Goods & Services | https://transparency.meta.com/policies/ad-standards/restricted-goods-services/health-wellness/ | Supplement/health ad restrictions — basis for eliminating whey protein |
| 30 | Flighted | How to Run Meta Ads for Supplement Brands in 2026 | https://www.flighted.co/blog/meta-ads-strategy-for-supplement-brands-2026 | 64%+ of supplement accounts face ad review in 2026 |
| 31 | ProPakistani | Pakistan Listed 7th for Highest Per Capita Tea Consumption | https://propakistani.pk/2018/06/25/its-tea-time-pakistan-listed-on-7th-for-highest-per-capita-tea-consumption/ | Tea-culture context (article from 2018 — dated, flagged) |
| 32 | World Tea News | Pakistan is Stocking Up on Global Tea | https://www.worldteanews.com/Insights/pakistan-stocking-global-tea | $611M tea imports, 172,911 tonnes consumption |
| 33 | Meta Ad Library (live API query) | Ads targeting Pakistan, multiple keyword queries | https://www.facebook.com/ads/library/ | Primary evidence source for every "real active ads found" claim throughout this report; queried 2026-09-19 |

---

*This report was produced using live Meta Ad Library queries, web search, and Daraz.pk listings on 2026-09-19. Market conditions, ad landscapes, and competitor activity in Pakistani e-commerce change quickly — treat figures more than a few months old at the time of reading as directional, not current, and re-verify before committing significant capital.*
