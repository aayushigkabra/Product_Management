# Fintech Growth Strategy: Tier-2 India

---

## The Question

400 million people in Tier-2 and Tier-3 India use UPI. 68% of them have no credit product. Most fintech companies know this and still treat "Tier-2 users" as a single persona, a single funnel, and a single GTM motion.

This project builds a full acquisition-to-habit growth strategy for a fintech product entering Bharat, starting from a question most strategies skip: who exactly is the user, and what do they actually need?

---

## Core Thesis

Tier-2 India is not one market. A 26-year-old salaried employee in Indore and a 38-year-old local grocery store owner in Coimbatore both live in Tier-2 cities. They need different products, different acquisition channels, and the unit economics for each are materially different.

The strategy is built around two personas, and every decision flows from that split.

---

## The Two Personas

### Rajan, 26 · Salaried user · Indore
- Earns Rs 28,000 a month, sends some home, has never used a credit product
- Uses UPI for peer-to-peer transfers only
- Finds KYC confusing; English-only interfaces lose him
- Acquisition trigger: a WhatsApp message from a friend, not an ad
- Device: Rs 12,000 Android, 4G, intermittent connectivity

### Meenakshi, 38 · Small business owner · Coimbatore
- Runs a local grocery store, accepts UPI but pays suppliers in cash
- Has over a year of UPI transaction history but no formal credit record
- Acquisition trigger: her FMCG distributor mentions an app that lends based on UPI history rather than collateral
- Language: Tamil. English is a barrier.
- Device: Rs 8,000 Android, feature-phone mindset

---

## Where the Funnel Breaks

A standard fintech funnel loses 80-85% of Tier-2 users before their first transaction. The drop-off is not at awareness. It is at KYC.

| Stage | Conversion | Key drop reason |
|---|---|---|
| Awareness / Install | 100% | App store friction, storage constraints |
| Onboarding start | 62% | KYC complexity, document confusion |
| KYC completed | 38% | Trust gap, no clear next step |
| Account activated | 20% | No compelling reason to transact |
| First transaction | 10% | No habit formed |
| D30 active | 5% | Loop never established |

**Priority fixes:**
- Video KYC in Hindi, Tamil, and Telugu
- WhatsApp-assisted KYC as a fallback
- Immediate value signal post-KYC (show credit limit or savings plan before asking for action)
- Rs 50-100 cashback on first transaction
- WhatsApp nudge 24h after KYC if no transaction

---

## Growth Levers (Ranked)

| # | Lever | Impact | Effort | Priority |
|---|---|---|---|---|
| 01 | WhatsApp referral loop | Very High | Low | P0 |
| 02 | Vernacular-first onboarding | High | Medium | P0 |
| 03 | Agent and assisted onboarding model | Very High | High | P0 |
| 04 | UPI transaction history as credit signal | Very High | Very High | P1 |
| 05 | Financial literacy content in local language | Medium | Low | P1 |
| 06 | Savings gamification (Rajan persona) | Medium | Medium | P2 |

### The lever most strategies miss: the agent model

Some of the strongest Tier-2 growth stories in Indian fintech came from assisted onboarding through local shop owners and Jan Seva Kendras, not digital ad spend. A trained local agent walks users through KYC in person, in their language, earning Rs 100 per completed onboarding.

CAC is higher at Rs 175 vs Rs 95 for the referral channel. But the LTV for the SMB persona is Rs 3,360 over 12 months. The unit economics hold.

### Vernacular is not just translation

Changing "credit score" to "financial trust score" in Hindi is a product decision, not a copy decision. It affects whether someone trusts the app enough to complete KYC. The strategy calls for full cultural adaptation across Hindi, Tamil, Telugu, and Kannada, including voice input for forms where typing is a barrier.

---

## Go-to-Market Approach

**City-first, then corridor, then national.** Launch in 3 anchor cities with strong UPI penetration, an active SMB base, and existing trust in digital payments. Prove the model before scaling.

**Anchor cities (Phase 1):** Indore, Coimbatore, Surat

**Expansion corridors (Phase 2):**
- Indore to Bhopal to Jabalpur
- Coimbatore to Madurai to Trichy
- Surat to Rajkot to Vadodara

**National (Phase 3):** Only after proven CAC and LTV in Phase 1 and 2 cities.

---

## Unit Economics

|  | Rajan (salaried) | Meenakshi (SMB) |
|---|---|---|
| CAC | Rs 95 | Rs 175 |
| ARPU (M6) | Rs 180 | Rs 420 |
| Gross margin | 62% | 58% |
| Payback period | 8 months | 7 months |
| 12-month LTV | Rs 1,440 | Rs 3,360 |
| LTV:CAC | 15:1 | 19:1 |

The SMB persona has higher CAC but significantly higher LTV. The agent channel costs more to run but serves the higher-value user. Running both channels in parallel is the right call.

---

## Success Metrics

**North star:** 5M monthly transacting users by month 18

**Acquisition:** CAC (blended) ≤ Rs 130 / KYC completion ≥ 55% / referral share of installs ≥ 40%

**Activation:** D1 transaction rate ≥ 35% / time to first transaction ≤ 24h

**Retention:** D30 retention ≥ 42% / M3 retention ≥ 28% / transactions per user per month ≥ 6

**Revenue:** ARPU at M6 ≥ Rs 220 / LTV:CAC ≥ 12:1 / credit NPA rate ≤ 4%

**Guardrails:** Support CSAT ≥ 4.1/5 / app crash rate ≤ 0.5% / fraud rate ≤ 0.1%

---

## What I'd Validate First

Two assumptions I'd want to test before scaling:

1. **Agent model CAC assumption.** The Rs 150-200 CAC estimate is based on reported costs from assisted onboarding programmes in Indian fintech from 2019-2021. Those numbers may have shifted. A 4-week agent pilot in one anchor city before committing to the full network build would confirm or revise this.

2. **Vernacular as a KYC conversion driver.** The strategy assumes vernacular UI materially improves KYC completion rates. This needs an A/B test: English UI vs Hindi UI vs voice-assisted UI on the same funnel. A 3-way split in week 1 of the pilot would give a clean answer.

---

## Roadmap

| Phase | Timeline | Focus |
|---|---|---|
| Phase 1 | Months 1-4 | Vernacular onboarding, WhatsApp referral, agent network pilot, Lite app |
| Phase 2 | Months 5-10 | Micro-savings product, UPI credit scoring, starter credit, corridor expansion |
| Phase 3 | Months 11-18 | National agent network, BNPL, insurance bundle, OTT advertising |


Part of a 7-project PM portfolio covering PRDs, growth strategy, experimentation, analytics, and teardowns.
