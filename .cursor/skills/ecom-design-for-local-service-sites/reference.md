# Evidence reference

Digest of design research on online stores for appointment-based service businesses (a men's barbershop with a third-party booking system, and a women's hair salon). Research notes dated **2026-11-11**.

Much of the data comes from booking, AI and salon-software vendors, so treat it as **directional**. Re-verify any figure before quoting it to a client. Confidence: **H** high, **M** medium, **L** low.

## Checks on earlier design notes

| Earlier idea | Verdict | Wording to use |
|---|---|---|
| Top banner gets attention | Supported (M). Nielsen Norman Group 2018 eye-tracking: 57% of viewing time above the fold, 74% within the first two screenfuls. | An AOV banner placed low on the first screen should still sit within the first two screens. |
| Video heroes lower revenue per user | No independent source found. | "Heavy video risks slow loads." Keep the original claim only if its source is cited. |
| Set end dates | Real deadlines supported, fake ones not (M). A plain "Order before 4 PM" line lifted revenue 27.1% in a 42-day test, on only 1,877 visitors. A large US study found countdown timers did not significantly increase purchases. | Use real, server-enforced cut-offs. Timers that reset on refresh erode trust. |
| "Dollar amount saved" | Needs a genuine reference price. | Check local consumer-law rules on "was" prices first. |
| Chat placement (bottom-right vs embedded) | No reliable data found. | Treat as a hypothesis to A/B test. |

## Both businesses

### Mobile and speed
- Beauty sees about 78% of traffic on mobile but only about 64% of revenue (M).
- Mobile conversion averages 1.94% vs 3.71% on desktop. Mobile cart abandonment is about 82% (M).
- Speed: a 0.1s gain can lift retail conversion by 8.4% (Deloitte for Google). Nuvemshop's LCP work gave an 8.9% mobile conversion gain (M).

### Reviews and trust
- 78% of salon and spa customers check online reviews before booking, rising to 93% for ages 33 to 44 (Zenoti 2024 survey, vendor data, M).

### AOV and shipping
- Baymard average cart abandonment 70.22%. About 40% of US shoppers who abandon with real buying intent blame added costs such as shipping and fees (M).
- Average free-shipping minimum for health and beauty is about $61 (M, currency and region unclear).
- Threshold 25 to 30% above current AOV: rule of thumb (L).
- A twelve-store cohort reported a 9 to 17% AOV lift from a live progress bar in the cart (L, small sample).

## Barbershop (booking-led)

- **Online booking share is the KPI.** Median barbershop books 36% of appointments online vs 68% for the top 10% (Zenoti, vendor). Mangomint's sample of 181,180 appointments showed 77.49% booked online (vendor, M). With a booking system already in place, the website's job is to push people into it.
- **No-shows:** Zenoti benchmark is 4% no-shows plus 4% cancellations, about 8% of booked appointments lost (M). One aggregate puts no-shows at 5 to 7% with deposits and 12 to 18% without (L).
- **Products:** in US men's hair care, shampoo, styling and hair-loss or scalp treatments are 67.6% of market value (M). Online channels enable subscription replenishment, which points to a small replenishable range with a reorder option.
- **Gap:** no reliable data on barbershop retail attach rates or men's online conversion. Use the shop's own POS and order history.

## Women's salon (recommendation-led)

- **Retail share:** typically 5 to 15% of salon revenue but one of the most profitable lines. Average retail is 11.9% of sales vs 12.0% for the top quartile, so retail share alone does not separate strong salons from average ones (M).
- **Category pressure:** salon product sales fell 9.8% in Q1 2026 and retail units were down 12.22% in August. Prestige haircare is expanding on Ulta, Sephora and Amazon (M). Do not compete on price. Stylist recommendation is the differentiator.
- **Timing:** only 13% of retail sales happen at a client's first appointment. Inference: a post-visit "your stylist's picks" email or page tied to the service received is where the online store earns its place (inference, M).
- **Older stat to verify:** a Professional Beauty Association study found 47% of consumers trust their stylist most for product information, and 71% of clients were not offered a product introduction. Undated, appears old (L).
- **Memberships:** Zenoti reports membership salons grew revenue and retention at four times the rate of non-membership salons (vendor, L to M).
- **Supply terms (not researched):** professional brands often restrict online resale by authorised salons. Check distributor agreements before planning a store.

## AI support and booking

- **Missed calls (Zenoti, vendor):** about 35% of calls go unanswered, 82% of those during business hours. 85% of callers who reach voicemail hang up. 46% of salon bookings happen outside operating hours. Zenoti claims its AI converts one in three missed calls into bookings (vendor claim, L to M). This is where the case for AI booking and support is strongest.
- **Shopping-assistant claims:** the popular "12.3% vs 3.1% conversion" figure is vendor data (Rep AI) and almost certainly reflects self-selection (L).
- **Gorgias, more careful (M):** about 1 in 7 assistant conversations ends in an attributed order. Assisted orders are 47% larger ($181 vs $123). The assistant influences about 1.9% of online revenue, and about 80% of attribution is the weakest kind. Refunds on assisted orders may run higher, and habitual-purchase categories benefit least. For replenishable hair products expect a modest sales effect. Coverage of booking questions is the bigger win.
- **Integration is the main technical question:** because the booking system is third-party, check whether it exposes availability and booking through an API. One AI-receptionist vendor lists Fresha, Mindbody, Booker and Square Appointments as supported. That list may not include the client's system.

## Weaker sources, left out of the rules

- "62% want exact pricing before booking" and "72% prefer to book online" came from a web-design agency's stats page and are not well sourced. Pricing transparency is still worth testing.

## Next steps the research recommends

- Collect each business's own data: online booking share, call volume, top-selling products, repeat purchase rate.
- Confirm the booking system's API and deposit support.
- Confirm distributor rules on online product sales.
- Decide what to A/B test first: chat placement, AOV banner position, progress bar threshold.

## Sources

- Nielsen Norman Group fold study (2018), summarised at https://www.bkomstudios.com/blog/the-fold/
- Nuvemshop LCP case study: https://web.dev/case-studies/nuvemshop
- Countdown timer evidence: https://cleancommit.io/blog/do-countdown-timers-work/
- Mobile benchmarks: https://visionary-marketing.co.uk/blog/mobile-marketing-statistics-2026
- Zenoti 2024 Salon and Spa Survey: https://www.zenoti.com/wp-content/uploads/2025/08/2024-Salon-and-Spa-Survey.pdf
- Free shipping and Baymard figures: https://ppc.land/free-shipping-threshold/ and https://eightx.co/blog/average-free-shipping-threshold-by-vertical
- Barbershop benchmarks: https://www.zenoti.com/thecheckin/barbershop-trends-2026 and https://www.mangomint.com/blog/barbershop-booking-statistics/
- US men's hair care market: https://www.kenresearch.com/united-states-men-hair-care-products-market
- Salon retail data: https://www.blog.selfnamed.com/business/why-salons-are-becoming-retail-brands and https://issuu.com/docs/3963a2776e17d3b2863fd10ebea540f1
- Professional hair care and e-commerce: https://www.glossy.co/beauty/as-professional-hair-care-grows-in-us-retail-and-e-commerce-davines-bets-on-old-school-salons/
- PBA retail study: https://www.salontoday.com/articles/facts-figures-trivia
- Zenoti membership and AI data: https://www.zenoti.com/en-uk/2026-beauty-and-wellness-benchmark-report-salon-edition-ungated and https://www.zenoti.com/blog/ai-agents-missed-call-salon-appointment
- Gorgias assistant benchmark: https://www.gorgias.com/research/ai-shopping-assistants-are-now-officially-influencing-sales
- Rep AI figures, as reported at https://www.clickpost.ai/blog/ai-in-ecommerce-statistics
