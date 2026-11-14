---
name: ecom-design-for-local-service-sites
description: Design guidance for adding or improving online product sales and booking hand-off on websites for appointment-based local businesses (barbershops, hair salons, similar). Use when writing or reviewing the design or "future state" section of a client website doc, planning an online store, retail range, AOV banner, free-shipping threshold, reviews placement, urgency or sale messaging, or an AI chat or booking assistant for a service business.
---

# Ecom Design for Local Service Sites

Evidence-backed design rules for small appointment-based businesses that also sell products online. Use it to write the **design section of a future-state doc**, not to prescribe a build.

Stay client-agnostic in anything tracked in the repo (see `.cursor/rules/client-agnostic.mdc`). Real client names and numbers are only for docs under `clients/`.

## Inputs to read first

1. The client's `current-state.md` (booking system, shop status, locations, observed problems).
2. [reference.md](reference.md) for the numbers behind each rule, with confidence labels and sources.
3. The archetype below that fits the business.

## The stance

The site is **one touchpoint, not the product**. Its job depends on the archetype:

| Archetype | Site's main job | Store's role |
|---|---|---|
| **Booking-led** (e.g. barbershop with a third-party booking system) | Push visitors into the booking system from every page | Small, replenishable range with a reorder option. Secondary. |
| **Recommendation-led** (e.g. multi-stylist salon with retail) | Book, then extend the visit with the stylist's product advice | Post-visit "your stylist's picks", not a price-led shop |
| **Hybrid** | Both, with booking first | Only if the supplier terms and owner data justify it |

Evidence tags below: **H** high, **M** medium, **L** low confidence. Details in [reference.md](reference.md).

## Design rules

### Every page
1. **Book button on every page**, in the header and at the end of content. Booking-led sites win by raising the share of appointments booked online (M).
2. **Mobile first.** Beauty traffic is mostly mobile but mobile converts worse and abandons more. Design the phone layout first and the desktop second (M).
3. **Speed budget over spectacle.** Heavy hero video risks slow loads. Speed gains show measurable conversion lifts. Do **not** claim "video lowers revenue", as no source was found (M).
4. **Reviews at the point of decision**: at the booking hand-off and on product pages, not only a homepage carousel. Most salon customers check reviews before booking (M).
5. **Offer on one line.** A single short promo or threshold message beats a block of copy on mobile.
6. **Capture the missed call.** Many calls go unanswered, most hang up at voicemail, and a large share of bookings happen outside hours. Click-to-book and a clear after-hours path matter more than chat polish (M, vendor data).

### Store, if there is one
7. **Put the AOV banner within the first two screens** (about three quarters of attention is spent there) (M).
8. **Free-shipping progress bar in the cart.** Start the threshold roughly 25 to 30% above current AOV, then tune it (L). Show shipping and fees **early**, as unexpected costs are a top abandonment reason (M).
9. **Honest urgency only.** A real cut-off ("order before 4 PM for same-day dispatch") works. Fake or resetting timers erode trust and countdown timers showed no significant lift in a large study. Enforce end times **server-side** (M).
10. **"Amount saved" needs a genuine reference price.** Check local consumer-law rules on "was" prices before designing it. Do not give legal specifics as fact.
11. **Small, replenishable range.** Shampoo, styling and scalp products dominate men's hair care. Offer a reorder or subscription option (M).
12. **Don't compete on price.** Professional product sales are under pressure and big retailers are expanding. The differentiator is the stylist's recommendation (M).
13. **Tie product to the service received.** Few retail sales happen at the first appointment, so a post-visit email or page ("your stylist's picks") is where the store earns its place (M, inferred).

### Service and support extras
14. **Deposits and no-shows.** Roughly 8% of booked appointments are lost to no-shows and cancellations. Ask whether the booking system supports deposits before designing around them (M, L for the deposit effect).
15. **Memberships** can be a site feature for recurring services (vendor data, treat as a hypothesis).
16. **AI chat or booking assistant**: coverage of booking and FAQ questions is the bigger win. Expect a modest product-sales effect, especially for habitual purchases. Do not quote the "12.3% vs 3.1%" figure (self-selection). Placement is **unproven**, so list it as an A/B test (L).
17. **Price transparency** is worth testing, but the common "most want exact pricing" stat is weak (L).

## Gates before designing the store

Do not write store features as decisions until these are answered. List them under open questions:

- [ ] **Supplier terms:** do distributors or brands restrict online resale by authorised salons? (not researched)
- [ ] **Booking system:** does it expose availability or booking through an API? Does it support deposits?
- [ ] **Owner data:** online-booking share, call volume, top-selling products, repeat-purchase rate. Their own POS beats public benchmarks.
- [ ] **Jurisdiction and consumer law:** confirm the country or region before stating legal specifics.
- [ ] **Cost view:** any paid tool needs the managed vs client-owned view (see `.cursor/rules/pricing-and-costs.mdc`). Do not quote vendor prices from memory.

## Writing the future-state design section

Use this shape. Keep it proportionate: a small site gets a short section.

```markdown
## Design direction

**Archetype and site job:** [booking-led | recommendation-led | hybrid], and why.

### Principles applied
| Principle | What it changes on this site | Confidence |
|---|---|---|

### Page and template changes
[Only what the principles justify. Reference current-state problems.]

### Store (if any)
- Range and role:
- Banner, threshold and cart behaviour:
- Shipping and returns messaging:
- Post-visit or reorder flow:

### Experiments (not decisions)
| Test | Hypothesis | Metric | Needs |
|---|---|---|---|

### Gates and open questions
[From the checklist above.]

### Cost view
[Managed vs client-owned, if any paid tool is involved.]
```

## Do not

- State vendor statistics as industry fact. Say "vendor data" and the confidence.
- Recommend a store because it is possible. If retail attach rate and supplier terms are unknown, say so and park it.
- Add features the owner must check daily.
- Copy a number from [reference.md](reference.md) into a client-facing document without re-verifying the source.
