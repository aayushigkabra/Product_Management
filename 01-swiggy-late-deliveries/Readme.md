# Reducing Late Deliveries on Swiggy  
**PM Portfolio Project #1 · PRD + Wireframes**

---

## Overview

Late deliveries are one of the fastest ways to lose user trust in food delivery. This project focuses on reducing delays through a combination of UX improvements and system-level optimizations.

**Goal:** Improve on-time delivery rate from **74% → 88% within 2 quarters**, while maintaining marketplace balance.

---

## Why This Matters

- **26% of orders are late** (vs. ~14% industry benchmark)  
- **₹85 cost per late order** (refunds, support, churn impact)  
- Users with **2+ late orders churn 3.1× faster**

Fixing delivery reliability directly improves retention and reduces operational cost.

---

## Problem Breakdown

Late deliveries fall into three primary buckets:

| Bucket | What’s Going Wrong |
|---|---|
| **Restaurant delays** | No real-time capacity visibility; restaurants accept orders when overloaded |
| **Rider delays** | Inefficient batching, long pickup wait times, overloaded riders |
| **ETA/system issues** | Static and overly optimistic ETAs that ignore real-world variability |

**Key insight:** This is not a single failure point — it’s a system-wide coordination problem.

---

## Strategy

Two parallel approaches:

1. **Reduce perceived pain (communication & trust)**
2. **Reduce actual delays (logistics & prediction)**

This project prioritizes trust-first interventions before deeper system changes.

---

## Proposed Solutions (Prioritized)

| # | Initiative | Why It Matters | Priority |
|---|---|---|---|
| 1 | **Proactive Delay Alerts** | Sets expectations early and reduces frustration | **P0** |
| 2 | **Dynamic ETA Engine** | Improves prediction accuracy using real-time signals | **P0** |
| 3 | **Smart Rider Batching** | Prevents rider overload and cascading delays | P1 |
| 4 | **Restaurant Capacity Signals** | Reduces overload at the source | P1 |

### Key Product Decision

**Delay alerts are prioritized over ETA accuracy improvements.**

- A late order with warning = acceptable  
- A late order without warning = trust-breaking  

Alerts can ship in weeks, while ETA improvements take months.  
The focus is to build trust first, then improve accuracy.

---

## What Needs Validation

### 1. Do users forgive delays if warned?
**Experiment:**
- Alert + coupon  
- Alert only  
- No alert  

**Metrics:** churn, repeat rate, CSAT

---

### 2. Can restaurant capacity signals scale?
- Risk: operational overhead for partners  
- Approach: pilot with top restaurants in a single city before rollout

---

## Success Metrics

### North Star
- On-time delivery rate → **88%**

### Core Metrics
- Late delivery rate ≤12%  
- ETA accuracy (±5 min) ≥82%  
- Delay alert open rate ≥55%

### Retention Metrics
- D30 retention (late-order users) +6 pp  
- Coupon redemption ≥40%

### Guardrails
- Rider earnings → no decrease  
- Restaurant order volume → no decrease  
- Cancellation rate → no increase  

---

## Product Experience (Wireframes)

### 1. Order Tracking
- ETA shown as a **range (e.g. 28–35 min)** instead of a fixed value  
- Improves expectation setting

### 2. Delay Alert
- Proactive notification  
- Updated ETA + reason  
- Auto-applied ₹50 coupon  

### 3. Post-Delivery Feedback
- Structured issue tagging  
- Reorder prompt with incentive  

See `/wireframes` folder for designs.

---

## Roadmap (20 Weeks)

| Phase | Timeline | Outcome |
|---|---|---|
| Discovery | Weeks 1–2 | Data validation and root cause alignment |
| Phase 1 | Weeks 3–6 | Delay alerts (A/B tested) |
| Phase 2 | Weeks 7–14 | Dynamic ETA engine rollout |
| Phase 3 | Weeks 15–20 | Rider batching + restaurant pilot |
| Scale | Weeks 21–24 | National rollout and iteration |
