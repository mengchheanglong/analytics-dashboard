# 2. Business-Owner Question Evaluation

**Purpose:** Explain in simple words why each of the 60 questions is or is not included in the current business-owner dashboard.

## How to read each evaluation

- **Decision** says whether the question appears on the current dashboard.
- **Priority** shows its importance: High, Medium, Low, or Future.
- **Data** shows whether Angkoro can answer it now: Current data, Partial, Needs rule, or Gap.
- **Status** says whether it is Selected, Supporting, Combined, on a Separate surface, Planned, or Not selected.
- **Why** gives the reason in plain language.
- **Dashboard item** appears only when the question is selected or combined into an approved item.

## Status labels

- **Selected:** Included in the current dashboard.
- **Supporting:** Useful in a report, drill-down, or investigation, but not on the current dashboard.
- **Combined:** Already answered inside another approved dashboard item.
- **Separate surface:** Useful, but belongs on another authorized page such as Finance.
- **Planned:** Consider later after the missing rule, data, history, or workflow exists.
- **Not selected:** Deliberately excluded from the current plan.

## A. Sales and paid demand

### BO-S01 — What was valid Paid Sales in the selected period, by currency?

**Decision:** Selected for the current dashboard.
**Priority:** High · **Data:** Current data · **Status:** Selected

**Why:** Paid Sales shows whether customers generated real paid business. It counts valid paid events rather than merely created orders.

**Dashboard item:** **Paid Sales** — Primary KPI.

### BO-S02 — How many distinct Paid Orders were recorded?

**Decision:** Selected for the current dashboard.
**Priority:** High · **Data:** Current data · **Status:** Selected

**Why:** Paid Orders shows how much order volume produced Paid Sales. Reading value and order count together is clearer than using an average alone.

**Dashboard item:** **Paid Orders** — Primary KPI.

### BO-S03 — How did Paid Sales and Paid Orders change from the matched previous period?

**Decision:** Not selected as a separate dashboard item.
**Priority:** High · **Data:** Current data · **Status:** Combined

**Why:** Matched comparison belongs inside S01 and S02.

**Combined into:** Paid Sales and Paid Orders — comparison context.

### BO-S04 — What was Average Paid Order Value?

**Decision:** Selected for the current dashboard.
**Priority:** Medium · **Data:** Current data · **Status:** Selected

**Why:** This shows whether paid business changed because customers placed larger or smaller paid orders. Keep it below Paid Sales and Paid Orders rather than as a headline KPI.

**Dashboard item:** **Average Paid Order Value** — Supporting metric.

### BO-S05 — How did paid business split between COD and online payment?

**Decision:** Not selected for the current dashboard.
**Priority:** Medium · **Data:** Current data · **Status:** Supporting

**Why:** COD versus online mix is useful in a payment-method report, but it does not create a separate immediate seller action on the main dashboard.

### BO-S06 — Which day produced the highest valid Paid Sales?

**Decision:** Not selected for the current dashboard.
**Priority:** Low · **Data:** Current data · **Status:** Supporting

**Why:** Useful pattern, but rarely first-screen action.

### BO-S07 — How much paid value was later refunded or reversed?

**Decision:** Not selected.
**Priority:** Low · **Data:** Partial · **Status:** Not selected

**Why:** Stakeholder requested removal; retain only for reconciliation.

### BO-S08 — How much profit or margin did the store make?

**Decision:** Not selected now.
**Priority:** Future · **Data:** Gap · **Status:** Planned

**Why:** Cost snapshots needed for defensible profit or margin.

## B. Orders and seller decisions

### BO-O01 — Which orders need the seller to accept or reject now?

**Decision:** Selected for the current dashboard.
**Priority:** High · **Data:** Current data · **Status:** Selected

**Why:** These orders still need seller action. Missing the decision deadline can cause automatic cancellation, so this queue is more useful than a historical status chart.

**Dashboard item:** **Orders Need Decision** — Action queue.

### BO-O02 — Which waiting order reaches its decision deadline first?

**Decision:** Not selected as a separate dashboard item.
**Priority:** High · **Data:** Current data · **Status:** Combined

**Why:** Earliest deadline is the sort rule for O01.

**Combined into:** Orders Need Decision — queue sorting.

### BO-O03 — How many orders were auto-cancelled because the seller missed the decision deadline?

**Decision:** Not selected for the current dashboard.
**Priority:** Medium · **Data:** Partial · **Status:** Supporting

**Why:** Historical preventable loss; durable machine reason still needed. Keep it for investigation rather than the main dashboard.

### BO-O04 — How were rejected orders distributed by reason?

**Decision:** Not selected for the current dashboard.
**Priority:** Medium · **Data:** Current data · **Status:** Supporting

**Why:** Rejection distribution by reason helps listing or policy review.

### BO-O05 — How many orders were cancelled by the customer, seller, or system?

**Decision:** Not selected for the current dashboard.
**Priority:** Medium · **Data:** Partial · **Status:** Supporting

**Why:** Actor fields exist, but system reasons need stronger coding. Keep it for investigation rather than the main dashboard.

### BO-O06 — How many orders expired before payment succeeded?

**Decision:** Not selected for the current dashboard.
**Priority:** Medium · **Data:** Current data · **Status:** Supporting

**Why:** Indicates payment/buyer-completion loss. Keep it for investigation rather than the main dashboard.

### BO-O07 — How many current orders are in each lifecycle status?

**Decision:** Not selected for the current dashboard.
**Priority:** Low · **Data:** Current data · **Status:** Supporting

**Why:** Navigation aid; raw statuses are not business outcomes.

### BO-O08 — How many COD orders were placed, accepted, and cash-collected?

**Decision:** Not selected for the current dashboard.
**Priority:** Medium · **Data:** Current data · **Status:** Supporting

**Why:** COD stage context is useful but not a separate top decision.

## C. Fulfillment and completion

### BO-F01 — Which accepted prepaid orders still need fulfillment?

**Decision:** Selected for the current dashboard.
**Priority:** High · **Data:** Current data · **Status:** Selected

**Why:** These accepted prepaid orders are paid customer commitments that remain unfinished. Keep them separate from seller-decision work because the required action is fulfillment.

**Dashboard item:** **Fulfillment Backlog** — Action queue.

### BO-F02 — Which fulfillment item has waited the longest?

**Decision:** Not selected as a separate dashboard item.
**Priority:** High · **Data:** Current data · **Status:** Combined

**Why:** Oldest item is the queue sort for F01.

**Combined into:** Fulfillment Backlog — queue sorting.

### BO-F03 — How long does fulfillment normally take after acceptance?

**Decision:** Not selected for the current dashboard.
**Priority:** Medium · **Data:** Current data · **Status:** Supporting

**Why:** Current timestamps can describe operating speed.

### BO-F04 — How many orders are overdue or fulfilled on time?

**Decision:** Not selected now.
**Priority:** Future · **Data:** Needs rule · **Status:** Planned

**Why:** `Overdue` and on-time rate require a fulfillment SLA.

### BO-F05 — How many orders reached completed status?

**Decision:** Not selected for the current dashboard.
**Priority:** Low · **Data:** Current data · **Status:** Supporting

**Why:** Throughput context, not usually the next decision.

## D. Products and inventory

### BO-I01 — Which product sold the most valid paid units?

**Decision:** Selected for the current dashboard.
**Priority:** Medium · **Data:** Current data · **Status:** Selected

**Why:** Ranking products by valid paid units supports stock and promotion decisions without becoming another headline KPI.

**Dashboard item:** **Top Products** — Breakdown.

### BO-I02 — Which product produced the most valid Paid Sales?

**Decision:** Not selected for the current dashboard.
**Priority:** Medium · **Data:** Current data · **Status:** Supporting

**Why:** Product-value contribution explains Paid Sales.

### BO-I03 — Which category produced the most valid Paid Sales?

**Decision:** Not selected now.
**Priority:** Future · **Data:** Partial · **Status:** Planned

**Why:** Historical category snapshots are not reliably preserved.

### BO-I04 — Which active products recorded no paid units?

**Decision:** Not selected for the current dashboard.
**Priority:** Low · **Data:** Current data · **Status:** Supporting

**Why:** Requires context for newly listed or intentionally inactive demand.

### BO-I05 — Which tracked products or variants need inventory attention because they are out of stock or low stock?

**Decision:** Selected for the current dashboard.
**Priority:** High · **Data:** Current data · **Status:** Selected

**Why:** Out-of-stock and low-stock items lead to the same action: restock or change availability. Keep the two states separate so the seller can see immediate shortages and near-term risk.

**Dashboard item:** **Inventory Attention** — Action queue.

### BO-I06 — Which open-order reservations reduce each item's available units?

**Decision:** Not selected for the current dashboard.
**Priority:** Medium · **Data:** Current data · **Status:** Supporting

**Why:** Reservation pressure explains availability.

### BO-I07 — Which best-selling item is also at inventory risk?

**Decision:** Not selected for the current dashboard.
**Priority:** Medium · **Data:** Current data · **Status:** Supporting

**Why:** Useful combination of paid demand and inventory risk.

### BO-I08 — How many days remain before an item runs out?

**Decision:** Not selected now.
**Priority:** Future · **Data:** Gap · **Status:** Planned

**Why:** Needs inventory history, demand window, and replenishment assumptions.

### BO-I09 — How much paid value may have been lost during stockouts?

**Decision:** Not selected now.
**Priority:** Future · **Data:** Gap · **Status:** Planned

**Why:** Needs stockout intervals and suppressed-demand evidence.

## E. Customers

### BO-C01 — How many identifiable customers placed a valid paid order?

**Decision:** Not selected for the current dashboard.
**Priority:** Medium · **Data:** Current data · **Status:** Supporting

**Why:** Useful only with explicit identifiable-customer coverage.

### BO-C02 — What percentage of identifiable paid customers purchased again?

**Decision:** Not selected for the current dashboard.
**Priority:** Medium · **Data:** Partial · **Status:** Supporting

**Why:** Repeat rate is limited by guest and mutable identity.

### BO-C03 — How many identifiable paid customers were new versus returning?

**Decision:** Not selected for the current dashboard.
**Priority:** Medium · **Data:** Partial · **Status:** Supporting

**Why:** New/returning classification depends on stable history.

### BO-C04 — Which city or province produced the most paid orders?

**Decision:** Not selected for the current dashboard.
**Priority:** Low · **Data:** Current data · **Status:** Supporting

**Why:** Local delivery/promotion context, not primary health.

### BO-C05 — What percentage of Paid Orders can be linked to a known customer?

**Decision:** Not selected for the current dashboard.
**Priority:** Medium · **Data:** Current data · **Status:** Supporting

**Why:** Required denominator warning for customer analytics. Keep it for investigation rather than the main dashboard.

### BO-C06 — Which identifiable customer produced the highest valid paid value?

**Decision:** Not selected for the current dashboard.
**Priority:** Low · **Data:** Partial · **Status:** Supporting

**Why:** Requires privacy-safe use and stable identity.

### BO-C07 — What is customer lifetime value?

**Decision:** Not selected now.
**Priority:** Future · **Data:** Gap · **Status:** Planned

**Why:** Stable identity and sufficient history are not yet reliable.

## F. Checkout and product payments

### BO-P01 — What percentage of complete online product-payment attempts succeeded?

**Decision:** Not selected now.
**Priority:** Future · **Data:** Partial · **Status:** Planned

**Why:** Complete payment-attempt denominator needs coverage audit.

### BO-P02 — How many online product-payment attempts failed?

**Decision:** Not selected for the current dashboard.
**Priority:** Medium · **Data:** Partial · **Status:** Supporting

**Why:** Failed payment rows help troubleshooting but may not be complete. Keep it for investigation rather than the main dashboard.

### BO-P03 — Which failure reason, provider, or method performs worst?

**Decision:** Not selected for the current dashboard.
**Priority:** Medium · **Data:** Partial · **Status:** Supporting

**Why:** Provider/method comparison needs comparable attempt coverage. Keep it for investigation rather than the main dashboard.

### BO-P04 — How long does a successful product payment normally take?

**Decision:** Not selected for the current dashboard.
**Priority:** Low · **Data:** Current data · **Status:** Supporting

**Why:** Payment timestamps can describe completion time.

### BO-P05 — At which tracked checkout step were carts abandoned?

**Decision:** Not selected now.
**Priority:** Future · **Data:** Gap · **Status:** Planned

**Why:** No authoritative cart/checkout-step event stream.

### BO-P06 — What percentage of storefront visits became valid Paid Orders?

**Decision:** Not selected now.
**Priority:** Future · **Data:** Gap · **Status:** Planned

**Why:** No trustworthy storefront-visit denominator.

## G. Finance and payouts

### BO-M01 — How much store money is currently available for payout?

**Decision:** Selected for the current dashboard.
**Priority:** Medium · **Data:** Current data · **Status:** Selected

**Why:** The owner's immediate cash question. Knowing what is available to withdraw right now is as useful as knowing Paid Sales. This is a current snapshot, not a period performance metric — show only the current available amount, not a trend, sparkline, or period comparison. The full money lifecycle (pending settlement, escrow, reserved for payout, paid out) remains on the authorized Finance page. COD cash stays with the seller outside the platform wallet.

**Dashboard item:** **Available Balance** — Current finance snapshot.

### BO-M02 — How much store money is pending settlement or held in escrow?

**Decision:** Not selected for this dashboard.
**Priority:** Medium · **Data:** Current data · **Status:** Separate surface

**Why:** Pending settlement or escrow explains why online Paid Sales may not yet be available. Keep this on the authorized Finance page; COD cash remains outside the platform wallet.

### BO-M03 — How much money is reserved for payout requests in progress?

**Decision:** Not selected for the current dashboard.
**Priority:** Medium · **Data:** Current data · **Status:** Supporting

**Why:** Prevents confusion between reserved and available money.

### BO-M04 — Which payout requests failed, and why?

**Decision:** Not selected for the current dashboard.
**Priority:** Medium · **Data:** Current data · **Status:** Supporting

**Why:** Direct payout recovery work belongs in finance.

### BO-M05 — How much money was successfully paid out?

**Decision:** Not selected for the current dashboard.
**Priority:** Low · **Data:** Current data · **Status:** Supporting

**Why:** Useful payout history, not daily commerce command.

### BO-M06 — How much seller money was reversed through refunds or settlement corrections?

**Decision:** Not selected for the current dashboard.
**Priority:** Low · **Data:** Current data · **Status:** Supporting

**Why:** Reconciliation information; not a general dashboard KPI. Keep it for investigation rather than the main dashboard.

## H. Store readiness

### BO-R01 — Is the store active and allowed to operate?

**Decision:** Combined into a current dashboard item.
**Priority:** Medium · **Data:** Current data · **Status:** Combined

**Why:** It contributes the operating-permission check and appears only when the store is not active or allowed to operate.

**Dashboard item:** **Store Readiness** — Conditional status.

### BO-R02 — Does the storefront have at least one active sellable product?

**Decision:** Combined into a current dashboard item.
**Priority:** Medium · **Data:** Current data · **Status:** Combined

**Why:** It contributes the sellable-product check and appears only when the storefront has no active product customers can buy.

**Dashboard item:** **Store Readiness** — Conditional status.

### BO-R03 — Can customers use at least one configured checkout method?

**Decision:** Combined into a current dashboard item.
**Priority:** Medium · **Data:** Current data · **Status:** Combined

**Why:** It contributes the checkout-method check and appears only when customers cannot use a configured payment method.

**Dashboard item:** **Store Readiness** — Conditional status.

### BO-R04 — Is the payout bank account verified?

**Decision:** Combined into a current dashboard item.
**Priority:** Medium · **Data:** Current data · **Status:** Combined

**Why:** It contributes the payout-readiness check while keeping sensitive bank details out of the dashboard summary.

**Dashboard item:** **Store Readiness** — Conditional status.

### BO-R05 — Are Telegram and order notifications connected and enabled?

**Decision:** Combined into a current dashboard item.
**Priority:** Medium · **Data:** Current data · **Status:** Combined

**Why:** It contributes the Telegram and order-notification check and appears only when seller response may be blocked.

**Dashboard item:** **Store Readiness** — Conditional status.

### BO-R06 — Are required contact and fulfillment settings complete?

**Decision:** Combined into a current dashboard item.
**Priority:** Medium · **Data:** Current data · **Status:** Combined

**Why:** It contributes the required contact and fulfillment-settings check and appears only while setup is incomplete.

**Dashboard item:** **Store Readiness** — Conditional status.

## I. Future and advanced analytics

### BO-A01 — Which traffic source produces the most valid paid business?

**Decision:** Not selected now.
**Priority:** Future · **Data:** Gap · **Status:** Planned

**Why:** Traffic-source attribution is not recorded.

### BO-A02 — Which campaign produces more value than it costs?

**Decision:** Not selected now.
**Priority:** Future · **Data:** Gap · **Status:** Planned

**Why:** Campaign cost and attribution are missing.

### BO-A03 — Which products are often purchased together?

**Decision:** Not selected now.
**Priority:** Future · **Data:** Current data · **Status:** Planned

**Why:** Current order items can support this analysis, but it is lower priority than the selected health and action questions. Keep it for later merchandising work.

### BO-A04 — What demand should the seller expect next?

**Decision:** Not selected now.
**Priority:** Future · **Data:** Gap · **Status:** Planned

**Why:** Forecasting needs reliable history, lead time, and evaluation.

### BO-A05 — Which unusual business change needs investigation?

**Decision:** Not selected now.
**Priority:** Future · **Data:** Partial · **Status:** Planned

**Why:** Needs approved baselines and enough history; cannot claim cause.

## Final dashboard items

1. **BO-S01 — Paid Sales** — Primary KPI
2. **BO-S02 — Paid Orders** — Primary KPI
3. **BO-M01 — Available Balance** — Current finance snapshot
4. **BO-O01 — Orders Need Decision** — Action queue
5. **BO-F01 — Fulfillment Backlog** — Action queue
6. **BO-I05 — Inventory Attention** — Action queue
7. **BO-S04 — Average Paid Order Value** — Supporting metric
8. **BO-I01 — Top Products** — Breakdown
9. **BO-R01–R06 — Store Readiness** — Conditional status

## Final decision

All 60 questions remain documented. The current dashboard includes only the approved items above; supporting, combined, separate-surface, and planned questions remain available here without crowding the dashboard. Available Balance appears as a current finance snapshot beside Paid Sales and Paid Orders — not as a matched-period performance KPI. The full money lifecycle (pending, escrow, reserved, paid out) and payout history remain on the authorized Finance page.

For the approved content definitions, use [03_Dashboard_Content.md](03_Dashboard_Content.md).
