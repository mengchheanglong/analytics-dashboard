# 3. Business-Owner Dashboard Content

## Type guide

| Type | Simple meaning |
|---|---|
| Primary KPI | Main business result |
| Current finance snapshot | Money available right now — not a period performance metric |
| Action queue | Work that needs attention |
| Supporting metric | Helps explain a main result |
| Breakdown | Ranks or divides a result |
| Conditional status | Appears only when a condition needs attention |

## Approved dashboard content

| ID | Dashboard item | Type | Placement |
|---|---|---|---|
| BO-S01 | Paid Sales | Primary KPI | Business health |
| BO-S02 | Paid Orders | Primary KPI | Business health |
| BO-M01 | Available Balance | Current finance snapshot | Business health |
| BO-O01 | Orders Need Decision | Action queue | Immediate operations |
| BO-F01 | Fulfillment Backlog | Action queue | Immediate operations |
| BO-I05 | Inventory Attention | Action queue | Immediate operations |
| BO-S04 | Average Paid Order Value | Supporting metric | Beneath business health |
| BO-I01 | Top Products | Breakdown | Beneath business health |
| BO-R01–R06 | Store Readiness | Conditional status | Only when setup is incomplete or blocked |

## Business health

### BO-S01 — Paid Sales

**Type:** Primary KPI · **Placement:** Business health  
**Answers:** What was valid Paid Sales in the selected period, by currency?

**Meaning:** The value of valid customer payments connected to paid product orders in the selected period.  
**Use:** Check whether real paid business is rising, falling, or absent. Read it beside Paid Orders and the previous-period comparison.  
**Important rule:** Count only successful product payments linked to an order with `paidAt`; exclude late captures without it. COD counts only after confirmed cash collection. Keep currencies separate. This is gross paid business before later refunds or reversals—not profit, wallet balance, payout value, or finalized accounting revenue—and it should link to authorized Finance details.

### BO-S02 — Paid Orders

**Type:** Primary KPI · **Placement:** Business health  
**Answers:** How many distinct Paid Orders were recorded?

**Meaning:** The number of distinct orders connected to valid customer payments in the same period as Paid Sales.  
**Use:** Read it beside Paid Sales to see whether movement came from order volume or order value.  
**Important rule:** Use the same valid paid population as Paid Sales. Do not count every created order or checkout attempt. A paid order remains counted after later lifecycle changes; COD counts only after confirmed cash collection.

### BO-M01 — Available Balance

**Type:** Current finance snapshot · **Placement:** Business health
**Answers:** How much store money is currently available for payout?

**Meaning:** The authorized wallet amount currently available to request for withdrawal, not bound to any selected period.
**Use:** Decide whether to request a payout. Read it beside Paid Sales, understanding that Paid Sales counts valid paid commerce while Available Balance shows withdrawable cash.
**Important rule:** This is a current-timestamp snapshot — do not apply the period selector, do not show a trend or percent change, and do not present it as a performance KPI. It is not profit, a bank payout, or Paid Sales. The full money lifecycle (pending settlement, escrow, reserved for payout, paid-out history) stays on the authorized Finance page. Link to Finance for the complete breakdown.

## Needs attention

### BO-O01 — Orders Need Decision

**Type:** Action queue · **Placement:** Immediate operations  
**Answers:** Which orders need the seller to accept or reject now?

**Meaning:** Paid prepaid orders not yet accepted and COD orders still waiting for the seller’s decision.  
**Use:** Work from the nearest decision deadline to prevent automatic cancellation.  
**Important rule:** This is not every open order, unpaid order, historical cancellation, or fulfillment task.

### BO-F01 — Fulfillment Backlog

**Type:** Action queue · **Placement:** Immediate operations  
**Answers:** Which accepted prepaid orders still need fulfillment?

**Meaning:** Valid prepaid orders the seller accepted but has not fulfilled.  
**Use:** Work oldest accepted orders first and watch whether paid customer commitments are building up.  
**Important rule:** Exclude orders waiting for acceptance, COD decision work, and fulfilled or completed orders. Show age, but do not call an order overdue until Angkoro adopts a fulfillment target.

### BO-I05 — Inventory Attention

**Type:** Action queue · **Placement:** Immediate operations  
**Answers:** Which tracked products or variants need inventory attention because they are out of stock or low stock?

**Meaning:** Two separate states based on available tracked quantity after reservations: **Out of Stock** at 0 or fewer units and **Low Stock** at 1–5 units.  
**Use:** Review Out of Stock first, then Low Stock; restock, correct inventory, review reservations, or change sellability.  
**Important rule:** The 1–5 rule is a simple v1 warning, not a demand forecast or product-specific reorder point. It may over-alert slow sellers and under-alert fast sellers.

## Supporting content

### BO-S04 — Average Paid Order Value

**Type:** Supporting metric · **Placement:** Beneath business health  
**Answers:** What was Average Paid Order Value?

**Meaning:** Paid Sales divided by Paid Orders for the same valid paid population, calculated separately for each currency.  
**Use:** Explain whether Paid Sales changed because paid orders became larger or smaller.  
**Important rule:** It is undefined when there are no Paid Orders. Do not combine currencies or present it as a headline KPI.

### BO-I01 — Top Products

**Type:** Breakdown · **Placement:** Beneath business health  
**Answers:** Which product sold the most valid paid units?

**Meaning:** Products ranked by units in valid paid orders during the selected period.  
**Use:** Identify proven demand for stock and promotion decisions.  
**Important rule:** Paid units are not Paid Sales, profit, margin, or a demand forecast. The ranking must follow the selected period.

## Conditional content

### BO-R01–R06 — Store Readiness

**Type:** Conditional status · **Placement:** Only when setup is incomplete or blocked  
**Answers:**

- BO-R01 — Is the store active and allowed to operate?
- BO-R02 — Does the storefront have at least one active sellable product?
- BO-R03 — Can customers use at least one configured checkout method?
- BO-R04 — Is the payout bank account verified?
- BO-R05 — Are Telegram and order notifications connected and enabled?
- BO-R06 — Are required contact and fulfillment settings complete?

**Meaning:** A setup checklist for conditions that may block selling, order handling, fulfillment, or payouts.  
**Use:** Show only failed or incomplete checks; hide the checklist when setup is complete.  
**Important rule:** Store Readiness is not a performance KPI and must not expose sensitive bank details.
