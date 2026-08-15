# Northstar Support Bot — Full Path Test Log
**Owner:** Timothy Kerre  
**Task Reference:** Board Task 13  
**Date:** Day 4–5  
**Total Paths Tested:** 15

---

## Testing Methodology

Each path was walked manually through the live Landbot bot using the preview mode. Results recorded as PASS / FAIL with notes.

---

## Category 1 — Order Status (6 paths)

| # | Path Description | Input Used | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|
| 01 | Happy path — shipped order with email | Order: NS-1002, Email: john.kamau@email.com | Shows "Shipped" + tracking number + ETA | Correct status returned | ✅ PASS |
| 02 | Happy path — delivered order with ZIP | Order: NS-1001, ZIP: 00100 | Shows "Delivered" + delivery date | Correct status returned | ✅ PASS |
| 03 | Delayed order | Order: NS-1004, Email: peter.otieno@email.com | Shows "Delayed" + new estimate | Delay message shown correctly | ✅ PASS |
| 04 | Processing order | Order: NS-1003, Email: amina.hassan@email.com | Shows "Processing" + estimated dispatch | Correct message shown | ✅ PASS |
| 05 | Invalid order ID format | Order: "ABC123" | Error message + prompt to recheck | Error handled, re-prompt shown | ✅ PASS |
| 06 | Order ID not found in dataset | Order: NS-9999 | Escalation to human support | Escalation triggered correctly | ✅ PASS |

---

## Category 2 — Returns & Refunds (5 paths)

| # | Path Description | Input Used | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|
| 07 | Happy path — eligible return | Order: NS-1001 | Eligible: yes + return instructions shown | Correct eligibility + steps shown | ✅ PASS |
| 08 | Ineligible return — final sale item | Order: NS-1009 | Ineligible: Final Sale policy explained | Policy shown, empathetic tone | ✅ PASS |
| 09 | Refund status — processed | Order: NS-1006 | "Refund processed on 2026-06-04" | Correct refund date shown | ✅ PASS |
| 10 | Refund status — in progress | Order: NS-1007 | "Return received — processing" | Correct in-progress message | ✅ PASS |
| 11 | Damaged item claim | Any order | Escalation to human team | Human takeover triggered | ✅ PASS |

---

## Category 3 — Stock Availability (4 paths)

| # | Path Description | Input Used | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|
| 12 | In-stock item by SKU | SKU: NS-BKPK-005, Black | "In stock — 15 units online" | Correct stock count returned | ✅ PASS |
| 13 | Out-of-stock item with restock date | SKU: NS-SHOE-001, Size 8 Blue | "Out of stock — restocks 10 Jun" | Correct out-of-stock + date | ✅ PASS |
| 14 | Out-of-stock — no restock date | SKU: NS-HDPH-002, White | "Out of stock — notify me option" | Notify Me option shown | ✅ PASS |
| 15 | Product name search (not SKU) | Product: "Yoga Mat", Purple | Inventory shown for Yoga Mat Purple | ⚠️ Partial — SKU lookup works but product name search returned no result | ❌ FAIL |

---

## Summary

| Category | Paths Tested | Passed | Failed |
|---|---|---|---|
| Order Status | 6 | 6 | 0 |
| Returns & Refunds | 5 | 5 | 0 |
| Stock Availability | 4 | 3 | 1 |
| **Total** | **15** | **14** | **1** |

---

## Known Failure — Path 15

**Issue:** Product name search in Stock Availability flow returns no result when user types a product name instead of SKU.  
**Root cause:** Landbot condition is checking for exact SKU match only.  
**Impact:** Low — customer is prompted to try SKU instead, which works correctly.  
**Recommended fix:** Add a secondary lookup by product name in the Landbot formula block.  
**Priority:** P2 — non-blocking for go-live.

---
*Test log owner: Timothy Kerre | Completed: Day 4*
