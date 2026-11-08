# Business Process Map

A lens for finding opportunities. For a typical appointment-based small business, the customer journey and the owner's operations break down roughly as follows. This is a map of **where to look**, not a list of things to build.

For each area, the useful questions are: *Where does time leak? Where do customers drop off? What does the owner dread or forget? What is done manually that doesn't need to be?*

## Customer-facing journey

| Process | Scope | Example pain points to probe |
|---------|-------|------------------------------|
| **Acquisition** | How new customers find the business: search, maps listings, social, word of mouth, walk-ins | Poor local visibility, outdated listings, no easy way to share the business |
| **Enquiry and booking** | Turning interest into a confirmed appointment | Back-and-forth messages, booking only during open hours, double bookings |
| **Pre-appointment** | Confirmations, reminders, preparation information | No-shows, last-minute cancellations, repeated questions |
| **Service delivery** | The appointment itself, check-in, queue, upsell | Walk-in management, running late, unclear pricing or service menu |
| **Payment** | Taking payment, deposits, tips, packages, gift cards | Cash-only friction, no deposits, manual invoicing |
| **Communication and support** | Answering questions and handling issues across channels | Same questions repeated, messages scattered across phone, DMs, email; slow replies out of hours |
| **Retention** | Getting customers to come back | No rebooking prompt, no loyalty or reactivation, no customer history |
| **Reputation** | Reviews, referrals, social proof | Few reviews, no process for asking, unanswered feedback |

## Behind-the-scenes operations

| Process | Scope | Example pain points to probe |
|---------|-------|------------------------------|
| **Scheduling and capacity** | Staff rosters, availability, time off, service durations | Calendar chaos, gaps in the day, manual updates |
| **Customer records** | Contact details, preferences, history, consent | Data in someone's phone, no single source of truth |
| **Inventory and suppliers** | Products sold or used in service | Stock-outs, manual reordering |
| **Staff management** | Onboarding, pay, performance, commissions | Spreadsheets, disputes |
| **Finance and admin** | Bookkeeping, tax, invoices, compliance | Receipts in a drawer, end-of-year panic |
| **Marketing** | Promotions, content, email/SMS, social posting | No time, inconsistent output |
| **Insights** | Knowing what is working | Decisions on gut feel, no visibility of busiest times or top services |

## Cross-cutting concerns

- **Channels**: website, phone, SMS, messaging apps, social DMs, email, in person
- **Data and privacy**: where customer data lives and who can access it
- **Integrations**: how systems talk to each other (or don't)
- **Owner attention**: how much ongoing effort the owner must spend

## Using the map

- Tag every idea, research note and process doc with a `process` value (see `.cursor/rules/doc-conventions.mdc`).
- Look for **handoffs between processes** (e.g. enquiry to booking to reminder to rebooking). Gaps there are often the highest-value opportunities.
- Expand or correct this map as we learn. It is a living document.
