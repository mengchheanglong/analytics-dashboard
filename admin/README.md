# Platform-Admin Dashboard — Stakeholder Summary

## Purpose

Help an authorized Angkoro platform administrator answer three simple things:

1. **Is the paid platform and merchant activity healthy?**
2. **What work needs administrator attention now?**
3. **Can the administrator trust the money, entitlements, and dashboard state?**

This page is the presentation view. The complete question register, decision reasoning, dashboard content, planned capability boundaries, and wireframe are linked below.

## Recommended dashboard

### Platform and merchant health

| Indicator | Plain-language answer | Why it matters |
|---|---|---|
| **Active Paid Stores** | How many stores currently have valid paid access | Monitors the usable paid-store base |
| **Subscription Collections** | How much valid subscription cash Angkoro collected, by currency | Monitors cash collected from paid subscriptions |
| **Platform Paid Orders** | How many valid paid orders occurred across stores | Shows whether merchants are generating paid demand |
| **Platform Paid Sales** | How much valid paid commerce occurred, by currency | Monitors merchant-commerce value across the platform |

### Immediate operations

| Indicator | Plain-language answer | Why it matters |
|---|---|---|
| **Payouts Awaiting Processing** | Which seller payouts still need processing | Prioritizes outstanding seller-money obligations |
| **Failed Payouts** | Which payout attempts failed and why | Routes failed money movement to recovery |
| **Bank Accounts Awaiting Verification** | Which payout accounts still need review | Unblocks safe seller payouts |
| **Renewals in Grace** | Which live subscriptions are at recoverable renewal risk | Supports renewal recovery without mislabeling Grace as churn |
| **Failed Onboarding Operations** | Which explicit onboarding operations failed | Routes failed store setup to retry or investigation |

### Control and integrity

| Indicator | Plain-language answer | Why it matters |
|---|---|---|
| **Wallet–Ledger Reconciliation** | Whether wallet balances agree with their ledgers | Detects money-integrity mismatches |
| **Plan Entitlement Integrity** | Whether paid plans have their intended features and limits | Detects access and configuration mismatches |
| **Dashboard Data Trust** | Whether dashboard data is fresh, complete, and full-population | Prevents stale or partial data from appearing trustworthy |
| **Source and Financial Reconciliation** | Whether an independent recomputation agrees with dashboard and authoritative records | Prevents a served aggregate from certifying itself |

## One-screen shape

```text
[ Active Paid Stores ] [ Collections USD / KHR ]
[ Paid Orders        ] [ Paid Sales USD / KHR   ]

[ Payouts Waiting ] [ Failed Payouts ] [ Bank Verification ]
[ Renewals in Grace ] [ Failed Onboarding ]

[ Data Trust — Fresh / Stale / Partial / Unknown ]
[ Conditional control alerts appear only when an issue or missing check exists ]
```

The four health indicators and five action queues are not equal cards. Health monitors the platform and queues lead to work. Data Trust remains visible as page-level source context; Wallet–Ledger Reconciliation, Plan Entitlement Integrity, and Source and Financial Reconciliation stay hidden or compact when clear and appear as alerts only for mismatch, affected, stale, unknown, or not-connected states.

## Supporting and conditional content

These explain primary outcomes or appear only when needed; they do not compete as equal headline cards:

- First Paid Subscriptions — supporting context beneath Active Paid Stores
- Stores Reaching First Paid Order — supporting context beneath merchant health
- Wallet–Ledger Reconciliation — conditional warning when a mismatch exists
- Plan Entitlement Integrity — conditional warning when access and configuration disagree
- Dashboard Data Trust — persistent freshness plus warning states
- Source and Financial Reconciliation — conditional warning for affected sections

Growth/payment maturity, reliability/recovery, security/incidents, and support/governance remain planned capability boundaries in `02_Evaluation.md`. They are not current dashboard widgets.

## Adopted v1 decisions

- **Reporting timezone:** `Asia/Phnom_Penh`
- **Currency:** Keep USD and KHR separate until Product and Finance approve the rate source, rate timestamp, rounding, and display policy required before any combined total
- **Current dashboard mode:** Only `Current data` content appears in `03`
- **Missing data:** Display `Unknown` or `Not connected`, never zero or healthy
- **Security:** Attack, WAF, anomaly, and incident monitoring remain planned until authoritative telemetry and workflows exist
- **Privacy:** Minimize user, session, bank, payment, and audit evidence and enforce least privilege
- **Seller autonomy:** Ordinary seller order decisions remain seller-owned

These are current analytical and placement decisions. Planned capabilities keep their reasons and readiness in `02` without crowding the current dashboard catalog.

## Delivery reality

The product facts support the 15 selected dashboard answers, but the current frontend does not implement this dashboard. Governed aggregates, reconciliation jobs, and the admin overview UI remain build work. Existing guarded payout and bank-account operations mean several action items need safe queue composition and UI integration rather than wholly new backend workflows.

The existing safe paginated bank-verification queue can be reused after adding oldest-first server sorting. The payout workflow has guarded by-ID operations but still needs a platform-wide work queue. AD-R07 cannot display a passing state until an independent reconciliation job exists and completes successfully. Reliability, security, support, and incident capabilities require the dependencies documented in `02` and the shared source audit.

No production values were calculated for this document.

## Documentation map

- [01 — Question register](./01_Questions.md) — all 66 stable IDs and full questions only; no evaluation reasoning
- [02 — Evaluation and decision record](./02_Evaluation.md) — plain Decision, Priority, Data, Status, Why, and selected dashboard item for every question
- [03 — Dashboard content](./03_Dashboard_Content.md) — complete catalog of the 15 approved current items
- [04 — Dashboard grouping and wireframe](./04_Dashboard_Grouping_and_Wireframe.md) — simple grouping, one overview wireframe, and a 15-item display guide
- [Shared source audit](../00_Source_Audit_and_Decisions.md) — verified product evidence, external research, and implementation boundaries

The evaluation page is self-contained. A reader does not need to switch to the question inventory to understand any decision.