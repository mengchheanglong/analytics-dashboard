# 3. Platform-Admin Dashboard Content

**Purpose:** Define the 15 items approved for the current platform-admin dashboard in plain language. Selection reasoning is in [02_Evaluation.md](./02_Evaluation.md); layout is in [04_Dashboard_Grouping_and_Wireframe.md](./04_Dashboard_Grouping_and_Wireframe.md).

## Type guide

| Type | Simple meaning |
|---|---|
| Primary KPI | Main platform result |
| Action queue | Work administrators need to handle |
| Supporting metric | Helps explain a main result |
| Conditional status | Shows freshness or appears when a control needs attention |

## Approved dashboard content

| ID | Dashboard item | Type | Placement |
|---|---|---|---|
| AD-G02 | Active Paid Stores | Primary KPI | Platform health |
| AD-S01 | Subscription Collections | Primary KPI | Platform health |
| AD-C01 | Platform Paid Orders | Primary KPI | Platform health |
| AD-C02 | Platform Paid Sales | Primary KPI | Platform health |
| AD-F01 | Payouts Awaiting Processing | Action queue | Attention indicators |
| AD-F03 | Failed Payouts | Action queue | Attention indicators |
| AD-F06 | Bank Accounts Awaiting Verification | Action queue | Attention indicators |
| AD-S07 | Renewals in Grace | Action queue | Attention indicators |
| AD-F08 | Wallet–Ledger Reconciliation | Conditional status | Trust & control |
| AD-O06 | Plan Entitlement Integrity | Conditional status | Trust & control |
| AD-R06 | Dashboard Data Trust | Conditional status | Trust & control |
| AD-R07 | Source and Financial Reconciliation | Conditional status | Trust & control |

AD-O01 (Failed Onboarding) appears only as a conditional alert when an explicit failure occurs. AD-S03 (First Paid Subscriptions) and AD-G05 (Stores Reaching First Paid Order) remain on the Analytics page.

## Platform health

### AD-G02 — Active Paid Stores

**Type:** Primary KPI · **Placement:** Platform and merchant health  
**Answers:** How many stores currently have valid paid access?

**Meaning:** Stores whose current subscription permits paid access, including stores in valid renewal Grace.  
**Use:** Monitor the usable paid-store base and compare it with the previous period.  
**Important rule:** Grace remains usable but must also appear in the renewal-risk queue. Do not include every created, trial, expired, suspended, or unpaid store.

### AD-S01 — Subscription Collections

**Type:** Primary KPI · **Placement:** Platform and merchant health  
**Answers:** How much valid subscription cash was collected, by currency?

**Meaning:** Valid paid subscription invoices collected during the selected period, separated by currency.  
**Use:** Monitor actual subscription cash collection beside Active Paid Stores.  
**Important rule:** This is operational collection data—not finalized accounting revenue, profit, or MRR. Never combine USD and KHR without an approved conversion policy.

### AD-C01 — Platform Paid Orders

**Type:** Primary KPI · **Placement:** Platform and merchant health  
**Answers:** How many valid Paid Orders occurred across Angkoro?

**Meaning:** Distinct product orders connected to valid customer payments across all stores in the selected period.  
**Use:** Monitor paid merchant demand and explain movement in Platform Paid Sales.  
**Important rule:** Count only successful product payments linked to an order with `paidAt`; exclude late captures without it. Use the full platform population, not a limited page of records. COD counts only after confirmed cash collection.

### AD-C02 — Platform Paid Sales

**Type:** Primary KPI · **Placement:** Platform and merchant health  
**Answers:** What valid Paid Sales occurred across Angkoro, by currency?

**Meaning:** Valid customer-payment value connected to paid product orders across all stores in the selected period.  
**Use:** Monitor merchant-commerce value beside Platform Paid Orders.  
**Important rule:** Use the same valid paid-event rule as Platform Paid Orders. Keep USD and KHR separate. This is not profit, wallet balance, payout value, or finalized accounting revenue.

## Needs attention

### AD-F01 — Payouts Awaiting Processing

**Type:** Action queue · **Placement:** Immediate operations  
**Answers:** Which payout requests await processing?

**Meaning:** Accepted seller payout requests that Angkoro has not yet processed.  
**Use:** Work oldest requests first and monitor count and value separately by currency.  
**Important rule:** Do not expose sensitive bank details or combine currencies.

### AD-F03 — Failed Payouts

**Type:** Action queue · **Placement:** Immediate operations  
**Answers:** Which payouts failed, and why?

**Meaning:** Failed payout attempts with safe operational reason context.  
**Use:** Investigate recoverable issues and route authorized recovery actions.  
**Important rule:** A failure is not proof of fraud or permanent loss. Minimize bank, provider, and seller details.

### AD-F06 — Bank Accounts Awaiting Verification

**Type:** Action queue · **Placement:** Immediate operations  
**Answers:** Which payout bank accounts await verification?

**Meaning:** Non-deleted payout bank accounts in the pending-verification state.  
**Use:** Review oldest pending accounts so valid sellers can become eligible for payouts.  
**Important rule:** Show only safe details such as the last four digits. Full account-number access requires authorization, step-up protection, and audit logging.

### AD-S07 — Renewals in Grace

**Type:** Action queue · **Placement:** Immediate operations  
**Answers:** Which live subscriptions are in renewal Grace?

**Meaning:** Stores whose paid subscription remains temporarily usable while renewal recovery is possible.  
**Use:** Prioritize the next Grace expiry and use the approved renewal-recovery process.  
**Important rule:** Grace is not churn, immediate expiry, or loss of access.

## Trust and control

### AD-F08 — Wallet–Ledger Reconciliation

**Type:** Conditional status · **Placement:** Control and integrity; only when mismatched  
**Answers:** Does every wallet balance reconcile with its ledger?

**Meaning:** Warns when a wallet balance and its supporting ledger entries disagree.  
**Use:** Keep a passing state compact; show affected wallets and the authorized reconciliation queue when mismatched.  
**Important rule:** A passing operational comparison is not accounting certification. Never hide missing records, failed checks, or differences behind a healthy state.

### AD-O06 — Plan Entitlement Integrity

**Type:** Conditional status · **Placement:** Control and integrity; only when mismatched  
**Answers:** Are active plans mapped to the intended features and limits?

**Meaning:** Compares live paid-plan access with the approved feature and limit catalog.  
**Use:** Warn only when access and configured entitlements disagree.  
**Important rule:** Do not infer intended limits from observed usage; compare with the approved plan catalog.

### AD-R06 — Dashboard Data Trust

**Type:** Conditional status · **Placement:** Page freshness and warning state  
**Answers:** Is dashboard data current, complete, and based on the full population?

**Meaning:** Shows whether dashboard data is current, complete, and connected to its sources.  
**Use:** Show freshness near the page heading and warn before administrators rely on affected content.  
**Important rule:** Missing, stale, failed, or incomplete data is `Unknown` or `Not connected`—never zero, healthy, or silently omitted.

### AD-R07 — Source and Financial Reconciliation

**Type:** Conditional status · **Placement:** Control and integrity; only when affected  
**Answers:** Do independently recomputed dashboard totals reconcile with authoritative source records and financial ledgers?

**Meaning:** An independent check comparing dashboard totals with authoritative operational and financial records.  
**Use:** Keep a passing state compact; when it fails, identify the affected section, check time, and failed source.  
**Important rule:** The dashboard query, cache, or aggregate cannot certify itself. If the independent check is missing, stale, or failed, show `Unknown` or `Not connected`. This remains broader than Wallet–Ledger Reconciliation and does not certify the accounting books.
