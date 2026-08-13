# Northstar Retail Co. — Ticket Taxonomy
**Owner:** Keith Ngugi  
**Status:** Complete ✅  
**Task Reference:** Board Task 04

---

## Overview

This document maps the 3 repetitive support ticket categories to real customer phrasings. Each category lists ≥ 8 documented phrasings sourced from common e-commerce support patterns (mocked for this sprint).

---

## Category 1 — Order Status

**Definition:** Any customer query about the current location, shipment status, or delivery timeline of a placed order.

**Trigger phrases:**
1. "Where is my order?"
2. "Has my order shipped yet?"
3. "I placed an order 3 days ago and haven't heard anything"
4. "What's the status of order #NS-1234?"
5. "My tracking number isn't working"
6. "When will my package arrive?"
7. "It says delivered but I haven't received anything"
8. "Has this been dispatched?"
9. "My order is showing as processing — is that normal?"
10. "I need my order by Friday — is that possible?"

**Resolution path:** Order ID + ZIP/email → check mock order dataset → return status + estimated delivery

**Escalation trigger:** Order marked delayed >5 days or delivered but not received

---

## Category 2 — Returns & Refunds

**Definition:** Any customer query about returning a product, checking return eligibility, or tracking a refund.

**Trigger phrases:**
1. "How do I return this?"
2. "I want to send something back"
3. "When will I get my refund?"
4. "Is this item eligible for a return?"
5. "I returned my item 2 weeks ago — no refund yet"
6. "Can I exchange this for a different size?"
7. "The item arrived damaged — what do I do?"
8. "I changed my mind — can I get my money back?"
9. "What is your return window?"
10. "Can I return a sale item?"

**Resolution path:** Order ID → check return eligibility → eligible: return instructions | ineligible: explain policy | refund status: check timeline

**Escalation trigger:** Return >30 days, damaged item claim, refund overdue >7 business days

---

## Category 3 — Stock Availability

**Definition:** Any customer query about whether a product, size, or colour variant is currently in stock or when it will be restocked.

**Trigger phrases:**
1. "Is this back in stock?"
2. "Do you have this in a size 8?"
3. "When will the blue version be available?"
4. "This says out of stock — when is it coming back?"
5. "Do you have this in a different colour?"
6. "Can I be notified when this is restocked?"
7. "Is this available in your store vs online?"
8. "I can't find my size — do you have it anywhere?"
9. "This SKU is showing unavailable"
10. "Is there a waitlist for this product?"

**Resolution path:** SKU / product name → check mock inventory dataset → in stock: confirm | out of stock: notify me option + restock estimate

**Escalation trigger:** Customer needs a guaranteed restock date or bulk order query

---

## Category Mapping Summary

| Category | Volume (mocked) | Avg Handle Time (human) | Bot Deflection Target |
|---|---|---|---|
| Order Status | 45% of tickets | 4 mins | 85% |
| Returns & Refunds | 35% of tickets | 7 mins | 70% |
| Stock Availability | 20% of tickets | 3 mins | 90% |

---
*Document owner: Keith Ngugi | Created: Day 1 | Reviewed: Day 2*
