# 4. Platform-Admin Dashboard Grouping and Wireframe

**Purpose:** Show the dashboard order and the simplest fitting display for each approved item. This is a proposed layout, not a completed interface.

## Dashboard groups

| Group | Approved items | Main question |
|---|---|---|
| Platform health | Active Paid Stores; Subscription Collections; Platform Paid Orders; Platform Paid Sales | Is the paid platform operating as expected? |
| Needs attention | Payouts Awaiting Processing; Failed Payouts; Bank Accounts Awaiting Verification; Renewals in Grace; Failed Onboarding Operations | What must administrators act on now? |
| Supporting | First Paid Subscriptions; Stores Reaching First Paid Order | Are stores progressing into paid activity? |
| Trust and control | Wallet–Ledger Reconciliation; Plan Entitlement Integrity; Dashboard Data Trust; Source and Financial Reconciliation | Can administrators trust the dashboard and money controls? |

## Simple wireframe

```text
+----------------------------------------------------------------------------+
| PLATFORM OVERVIEW               Period | Currency | Last updated             |
+----------------------------------------------------------------------------+
| Active Paid Stores | Subscription Collections | Paid Orders | Paid Sales     |
+----------------------------------------------------------------------------+
| SUPPORTING                                                                  |
| First Paid Subscriptions          | Stores Reaching First Paid Order         |
+----------------------------------------------------------------------------+
| NEEDS ATTENTION                                                             |
| Payouts Awaiting | Failed Payouts | Bank Verification | Grace | Onboarding   |
+----------------------------------------------------------------------------+
| DATA TRUST: Fresh / Stale / Partial / Unknown                               |
| Other control alerts appear only when an issue needs attention.             |
+----------------------------------------------------------------------------+
```

On smaller screens, show platform health first, then needs attention, supporting content, and trust/control alerts.

## Display guide

| ID | Dashboard item | Simple display |
|---|---|---|
| AD-G02 | Active Paid Stores | KPI card with previous-period comparison |
| AD-S01 | Subscription Collections | USD/KHR KPI card with trend |
| AD-C01 | Platform Paid Orders | Count card with trend |
| AD-C02 | Platform Paid Sales | USD/KHR KPI card with trend |
| AD-F01 | Payouts Awaiting Processing | Oldest-first queue with currency-separated context |
| AD-F03 | Failed Payouts | Recovery queue with safe failure reason |
| AD-F06 | Bank Accounts Awaiting Verification | Verification queue with safe bank details |
| AD-S07 | Renewals in Grace | Queue sorted by next expiry |
| AD-O01 | Failed Onboarding Operations | Failure and retry queue |
| AD-S03 | First Paid Subscriptions | Small supporting trend |
| AD-G05 | Stores Reaching First Paid Order | Small supporting trend |
| AD-F08 | Wallet–Ledger Reconciliation | Conditional warning and mismatch queue |
| AD-O06 | Plan Entitlement Integrity | Conditional warning and affected-plan list |
| AD-R06 | Dashboard Data Trust | Small persistent freshness status; warning when stale or incomplete |
| AD-R07 | Source and Financial Reconciliation | Conditional warning and affected-section list |

## Important rules

- Keep USD and KHR separate.
- Show the selected period and when the data was last updated.
- Action queues open only authorized administrator workflows.
- Keep non-data-trust control alerts hidden when no issue exists.
- Show a missing, stale, or failed source as `Unknown` or `Not connected`, never as Passed.
- Use `03_Dashboard_Content.md` for definitions and guardrails; do not repeat them here.
