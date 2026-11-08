# Pricing and Service Models

How we think about charging for anything that costs us money to run, such as email delivery (e.g. Resend), file/image storage (e.g. UploadThing), hosting, databases, messaging APIs, or AI usage. Vendor names here are examples of *categories*, not recommendations.

> This is a framework, not a price list. Vendor prices change often, so look up current pricing from the vendor and record the date. Never quote a vendor's price from memory. Currency, tax (e.g. GST/VAT) and legal terms are **not yet confirmed**. See open questions at the bottom.

## Core principle

**A feature is not viable until we know what it costs per client per month and what we'd charge for it.** Every idea in `ideas/` should have at least a rough answer.

## The two service models

### 1. Managed (we own it)

We hold the accounts, pay the vendors, and run the service. The client pays us a recurring fee.

- We carry the vendor bills, usage risk and uptime responsibility.
- The fee covers: vendor costs, our support time, a risk buffer, and margin.
- Good for non-technical owners, which is most of our clients. Creates recurring revenue and stickiness.
- Risks: usage spikes eat margin, vendor price rises land on us, and offboarding is on us.

### 2. Client-owned (they own it)

The client holds the accounts (hosting, email provider, storage, etc.) and pays vendors **directly**. We build and configure it.

- We charge a **setup fee**, plus optional paid support or maintenance, on a time or retainer basis.
- No vendor cost risk for us. Cleaner handover, and they can leave without friction.
- Risks: the client may change settings, let billing lapse, or share credentials badly, then expect us to fix it for free. Lower recurring revenue.
- Needs clear written boundaries on what support is and isn't included.

### 3. Hybrid (often the practical middle)

The client owns the accounts, we hold delegated access, and we charge a management fee for maintenance and monitoring. Vendor bills go to the client. Worth considering as the default "client-owned" variant for clients who want ownership but don't want to touch it.

### Comparison

| | Managed | Client-owned | Hybrid |
|---|---|---|---|
| Who owns accounts | Us | Client | Client |
| Who pays vendors | Us (recovered via fee) | Client | Client |
| Our revenue | Recurring, includes margin on costs | Setup fee, plus optional support | Setup fee, plus management fee |
| Our cost risk | High | None | None |
| Client effort | Lowest | Highest | Low |
| Lock-in / exit ease | Higher lock-in, we manage handover | Easy exit | Easy exit |
| Support load on us | Highest, we own all failures | Variable, depends on scope | Medium |

## Building up a price (managed model)

For each client, per month:

```
Vendor cost (fixed + expected usage)
+ Payment processing fees, if we bill through a processor
+ Support/maintenance time  (hours per month x our effective hourly rate)
+ Risk buffer               (usage spikes, price rises, failures)
+ Margin / overhead         (tools we use, admin, taxes, our own time on billing)
= Minimum viable monthly price
```

Then sanity-check it against **what the client will actually pay** (see "Client-side check" below). If the minimum viable price exceeds willingness to pay, the idea needs a cheaper option or isn't viable.

### Things that change the vendor cost

- **Pricing shape**: flat per account, per seat, per message/email/GB, or tiered. Know which, and model both a typical month and a bad month.
- **Free tiers**: useful for experiments, but **don't price a client service on a free tier** unless we've confirmed limits, terms and commercial-use rules. Price as if on the paid plan we'd realistically need.
- **Shared vs per-client accounts**: one shared vendor account across clients is cheaper but weakens data separation, makes cost attribution harder, and complicates offboarding. A per-client account costs more but is cleaner. Decide deliberately and record why.
- **Usage drivers**: what causes usage to grow (number of customers, appointments, messages, image uploads)? Is it predictable or spiky?
- **Fixed minimums**: vendors that bill a flat monthly minimum make small clients expensive.
- **Volume breaks**: costs per unit that fall at scale help us at 20 clients, but not at 2.
- **Currency**: many vendors bill in USD, so exchange rates affect margin.

## Protecting margin

- Include a **fair-use limit** (e.g. messages, storage, or requests per month) in the managed fee, with a stated overage rate or an upgrade tier.
- Reserve the right to **adjust pricing** with notice when vendor costs change.
- Prefer **flat, predictable client pricing** over pass-through billing, unless usage is highly variable. Owners like predictable bills.
- Where usage is genuinely variable, consider **pass-through at cost plus a handling fee**, or tiers.
- Track **actual cost per client** periodically so we notice a client who costs more than they pay.

## Client-side check

- What does the owner already spend on comparable tools or labour (e.g. paying a receptionist, booking apps, social media)?
- Does the price sit **below the value** they'd see (e.g. a few recovered appointments pay for it)?
- Is it clearly **separate** from the website fee, so the value is visible and the line item is easy to justify?
- Is there a **good / better / best** option so a tight-budget client can say yes to something?

## Handover and exit (matters for both models)

- Document where each client's accounts, data and credentials live.
- For managed: define what a client can take with them (data export, domain, content) and what is ours (our code, templates, tooling) in the agreement.
- For client-owned: agree who is responsible if a vendor bill lapses or a key is rotated.
- Make offboarding cheap for us to run. Keep it a checklist, not a project.

## Illustrative example (fictional numbers, not real prices)

An imaginary managed add-on that uses a hypothetical "Service X" for sending messages:

| Line | Per client / month |
|------|--------------------|
| Service X cost, typical usage | $4 |
| Share of fixed minimum | $2 |
| Payment processing | $1 |
| Support, 20 minutes at $60/hr | $20 |
| Risk buffer (about 20% of costs) | $5 |
| **Minimum viable price** | **about $32** |

If the owner would only pay $15 a month, either find a way to cut support time to nearly zero, drop features, or don't sell it as a managed service. Note that **support time usually dominates**, not the vendor bill. Cutting the vendor cost from $4 to $2 matters far less than preventing a single support call.

## Questions to answer for every idea that has third-party costs

1. What vendors and services are needed, and what is each one's current pricing shape? (Cite and date.)
2. What is the cost per client per month at typical and high usage?
3. Shared or per-client vendor accounts?
4. What would the managed price be, and what would the client-owned setup and support pricing be?
5. What fair-use limits protect us?
6. What happens when a vendor raises prices or changes terms?
7. What is the exit/handover story?
8. Is there a free or very cheap alternative that is good enough?

## Open questions

- Currency and tax treatment (e.g. whether GST applies to add-on services)
- Our target effective hourly rate and minimum margin
- Whether we bill vendor costs separately or bundle them into one retainer
- Contract and terms-of-service wording for both models (needs professional advice)
- Policy for clients who want to migrate from managed to client-owned later
