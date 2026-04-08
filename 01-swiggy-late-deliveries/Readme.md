# Reducing Late Deliveries on Swiggy

## The Problem

26% of Swiggy orders arrive after their promised ETA - nearly double the industry average of 14%. Each late delivery costs ~₹85 in compensation, support, and lost repeat business. Users who experience two or more late orders in a month churn at 3.1x the baseline rate.

**This PRD proposes a product intervention to bring the on-time delivery rate from 74% to 88% within two quarters.**

---

## Root Cause Analysis

Most PM write-ups jump straight to "build a better ETA model." I started with a fishbone analysis first.

Late deliveries break into three distinct failure modes:

| Cause Bucket | Key Root Causes |
|---|---|
| **Restaurant delay** | No live capacity signal to Swiggy; restaurants accept orders when overwhelmed |
| **Rider delay** | Poor batching logic; long pickup waits; multiple simultaneous deliveries |
| **System/ETA delay** | Static ETA ignores traffic, weather, prep time variance; optimistic ETAs to win orders |

---

## Proposed Solutions (Prioritised)

| # | Initiative | Impact | Effort | Priority |
|---|---|---|---|---|
| 1 | **Proactive Delay Alerts** - push notification + auto-coupon when delay >= 5 min | -4 pp churn after late order | Low | **P0** |
| 2 | **Dynamic ETA Engine** - ML model using traffic, weather, restaurant prep history | -8 pp late delivery rate | High | **P0** |
| 3 | **Smart Rider Batching** - limit concurrent deliveries based on distance model | -4 pp late delivery rate | Medium | P1 |
| 4 | **Restaurant Capacity Signal** - real-time prep time API, auto-pause on overload | -3 pp late delivery rate | High | P1 |

### Key prioritisation decision

I ranked **proactive alerts above the ML ETA engine** despite lower direct impact on the late-delivery rate.

Reason: a late delivery a customer was warned about is forgiven; one they weren't warned about causes churn.

Alerts ship in 3-4 weeks. The ML model ships in 3-4 months.

You build trust first, accuracy second.

---

## What I Would Validate First

Two assumptions in this PRD I'd want to pressure-test before building:

1. **"Users forgive delays if warned"**  
   This is backed by general UX research but I'd want Swiggy-specific data.  
   A/B test: delay alert with coupon vs delay alert without coupon vs no alert.

2. **"Restaurant capacity signal is feasible at scale"**  
   Getting 500K+ restaurant partners to update a real-time prep-time field is a significant change management challenge.  
   I'd pilot with 50 top partners in one city before building the full API.

---

## Success Metrics

**North star:** On-time delivery rate -> 88% (from 74%)

**Primary metrics:**
- Late delivery rate <= 12%
- ETA accuracy (within +/- 5 min) >= 82%
- Delay alert open rate >= 55%

**Retention metrics:**
- D30 retention for late-order users +6 pp
- Post-delay coupon redemption >= 40%

**Guardrail metrics** *(must not regress)*:
- Rider earnings per hour - no decrease
- Restaurant order volume - no decrease
- Order cancellation rate - no increase

---

## Wireframes

Three key screens in the intervention flow:

1. **Order tracking** - Live map with range ETA ("28-35 min") instead of a point estimate  
2. **Delay alert** - Proactive banner with updated ETA, reason, and auto-generated ₹50 coupon  
3. **Post-delivery feedback** - Structured tagging (late delivery, cold food, etc.) + coupon reorder prompt  

See `wireframes/` folder for annotated screen designs.

---

## Roadmap (20 weeks)

| Phase | Timeline | Deliverable |
|---|---|---|
| Discovery | Weeks 1-2 | Data audit, stakeholder alignment, root cause quantification |
| Phase 1 | Weeks 3-6 | Proactive delay alert system (A/B tested on 10% of delayed orders) |
| Phase 2 | Weeks 7-14 | Dynamic ETA Engine - shadow mode -> 5% -> 25% -> full rollout |
| Phase 3 | Weeks 15-20 | Smart rider batching + restaurant capacity signal pilot (Bangalore) |
| Scale | Weeks 21-24 | National rollout, metrics review, Phase 2 planning |

---
