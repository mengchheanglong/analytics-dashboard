# 2. Platform-Admin Question Evaluation

**Purpose:** Explain in simple words why each of the 66 questions is or is not included in the current platform-admin dashboard.

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

## A. Platform growth and store activity

### AD-G01 — How many stores are active and allowed to operate?

**Decision:** Not selected for the current dashboard.
**Priority:** Medium · **Data:** Current data · **Status:** Supporting

**Why:** Operational store count mixes paid and unpaid contexts.

### AD-G02 — How many stores currently have valid paid access?

**Decision:** Selected for the current dashboard.
**Priority:** High · **Data:** Current data · **Status:** Selected

**Why:** Monitors the usable paid-store base and its equal-period movement. `GRACE` remains usable but must also appear in the risk queue.

**Dashboard item:** **Active Paid Stores** — Primary KPI.

### AD-G03 — How many new stores were created and activated?

**Decision:** Not selected for the current dashboard.
**Priority:** Medium · **Data:** Current data · **Status:** Supporting

**Why:** Distinguishes account creation from stores that became operational.

### AD-G04 — What percentage of created stores became active?

**Decision:** Not selected now.
**Priority:** Future · **Data:** Partial · **Status:** Planned

**Why:** Reliable activation transition time/history is incomplete.

### AD-G05 — How many stores reached their first valid paid order?

**Decision:** Not selected for the current dashboard.
**Priority:** Medium · **Data:** Current data · **Status:** Separate surface

**Why:** First-paid-order activation is a merchant-growth signal for product and analytics review, not a daily admin action. Keep it on the Analytics page.

### AD-G06 — How long does a new store take to reach its first valid paid order?

**Decision:** Not selected now.
**Priority:** Future · **Data:** Partial · **Status:** Planned

**Why:** First-paid-order timing needs governed first-event logic.

### AD-G07 — Which active stores have no recent Paid Orders?

**Decision:** Not selected now.
**Priority:** Future · **Data:** Needs rule · **Status:** Planned

**Why:** `Recent` needs an adopted inactivity window and owner action.

### AD-G08 — What percentage of active stores have Telegram enabled?

**Decision:** Not selected for the current dashboard.
**Priority:** Low · **Data:** Current data · **Status:** Supporting

**Why:** Important channel adoption context, not core paid health.

## B. Platform commerce activity

### AD-C01 — How many valid Paid Orders occurred across Angkoro?

**Decision:** Selected for the current dashboard.
**Priority:** Medium · **Data:** Current data · **Status:** Selected

**Why:** Shows whether merchants are generating valid paid demand across Angkoro. Count valid paid orders, not every order or a limited page of records.

**Dashboard item:** **Platform Paid Orders** — Primary KPI.

### AD-C02 — What valid Paid Sales occurred across Angkoro, by currency?

**Decision:** Selected for the current dashboard.
**Priority:** Medium · **Data:** Current data · **Status:** Selected

**Why:** Shows valid commerce value across stores. Keep USD and KHR separate and exclude payments that did not become valid sales.

**Dashboard item:** **Platform Paid Sales** — Primary KPI.

### AD-C03 — How is the seller-decision backlog distributed across stores?

**Decision:** Not selected for the current dashboard.
**Priority:** Medium · **Data:** Current data · **Status:** Supporting

**Why:** Reveals platform-wide accumulation of orders waiting for seller decisions.

### AD-C04 — How many accepted prepaid orders await fulfillment?

**Decision:** Not selected for the current dashboard.
**Priority:** Medium · **Data:** Current data · **Status:** Supporting

**Why:** Reveals accepted prepaid orders that still await seller fulfillment.

### AD-C05 — How many orders expired before payment succeeded?

**Decision:** Not selected for the current dashboard.
**Priority:** Medium · **Data:** Current data · **Status:** Supporting

**Why:** Exposes checkout or payment friction without claiming an exact funnel drop-off.

### AD-C06 — Which stores produced the most valid Paid Orders?

**Decision:** Not selected for the current dashboard.
**Priority:** Low · **Data:** Current data · **Status:** Supporting

**Why:** Seller concentration context, not direct admin action.

### AD-C07 — How many orders auto-cancelled because sellers missed decision deadlines?

**Decision:** Not selected for the current dashboard.
**Priority:** Medium · **Data:** Partial · **Status:** Supporting

**Why:** Useful service-quality signal; durable reason code still needed. Keep it for investigation rather than the main dashboard.

## C. Subscriptions and monetization

### AD-S01 — How much valid subscription cash was collected, by currency?

**Decision:** Selected for the current dashboard.
**Priority:** High · **Data:** Current data · **Status:** Selected

**Why:** Shows actual paid subscription collections. Keep currencies separate and do not present this operational value as finalized accounting revenue.

**Dashboard item:** **Subscription Collections** — Primary KPI.

### AD-S02 — How are Active Paid Stores distributed across plans?

**Decision:** Not selected for the current dashboard.
**Priority:** Medium · **Data:** Current data · **Status:** Supporting

**Why:** Explains the composition of the paid-store base and plan exposure.

### AD-S03 — How many stores reached their first valid paid subscription?

**Decision:** Not selected for the current dashboard.
**Priority:** Medium · **Data:** Current data · **Status:** Separate surface

**Why:** First-subscription acquisition is a growth metric for product and analytics review, not a daily admin action. Keep it on the Analytics page.

### AD-S04 — How many stores are currently in a free trial?

**Decision:** Not selected for the current dashboard.
**Priority:** Low · **Data:** Current data · **Status:** Supporting

**Why:** Trial population is context, not paid health.

### AD-S05 — What percentage of ended trials became paid subscriptions?

**Decision:** Not selected now.
**Priority:** Future · **Data:** Partial · **Status:** Planned

**Why:** Needs immutable trial-end/paid-transition cohort logic.

### AD-S06 — Which trials end next?

**Decision:** Not selected for the current dashboard.
**Priority:** Medium · **Data:** Current data · **Status:** Supporting

**Why:** Actionable only if the team owns trial-expiry outreach.

### AD-S07 — Which live subscriptions are in renewal Grace?

**Decision:** Selected for the current dashboard.
**Priority:** High · **Data:** Current data · **Status:** Selected

**Why:** Identifies paid stores at recoverable renewal risk. `GRACE` still has valid access; it is not equivalent to churn or expiry.

**Dashboard item:** **Renewals in Grace** — Action queue.

### AD-S08 — How many first subscription payments failed before activation?

**Decision:** Not selected for the current dashboard.
**Priority:** Medium · **Data:** Current data · **Status:** Supporting

**Why:** Separates acquisition-payment failures from renewal problems.

### AD-S09 — What is monthly recurring subscription value?

**Decision:** Not selected now.
**Priority:** Future · **Data:** Needs rule · **Status:** Planned

**Why:** Recurring value is required for sustainability planning, but active-state, timing, and currency treatment must be adopted first.

### AD-S10 — What percentage of paid stores stopped subscribing?

**Decision:** Not selected now.
**Priority:** Future · **Data:** Gap · **Status:** Planned

**Why:** Retention is a core platform outcome, but Angkoro needs reliable historical cohorts and a governed churn event.

### AD-M01 — What operational platform-fee amount was recognized, by currency and source?

**Decision:** Not selected for the current dashboard.
**Priority:** Medium · **Data:** Current data · **Status:** Supporting

**Why:** Current commerce and payout fees are set to zero. Keep this in the Finance report unless Angkoro adopts a non-zero fee policy and needs recurring oversight; do not call it finalized accounting revenue.

## D. Payment and checkout reliability

### AD-P01 — What percentage of complete product-payment attempts succeeded?

**Decision:** Not selected now.
**Priority:** Future · **Data:** Partial · **Status:** Planned

**Why:** Checkout reliability is a platform responsibility, but the complete-attempt denominator and lifecycle coverage are not yet governed.

### AD-P02 — What percentage of complete subscription-payment attempts succeeded?

**Decision:** Not selected now.
**Priority:** Future · **Data:** Partial · **Status:** Planned

**Why:** Subscription collection reliability affects access and retention, but complete-attempt coverage is not yet governed.

### AD-P03 — Which failure reason, provider, or method performs worst?

**Decision:** Not selected now.
**Priority:** Medium · **Data:** Partial · **Status:** Planned

**Why:** Provider, method, and reason composition is needed to locate payment failures, but reason coverage and comparability remain incomplete.

### AD-P04 — Which payments have remained pending longer than expected?

**Decision:** Not selected now.
**Priority:** Future · **Data:** Needs rule · **Status:** Planned

**Why:** `Pending too long` requires method-specific limits.

### AD-P05 — How long does successful payment normally take?

**Decision:** Not selected for the current dashboard.
**Priority:** Low · **Data:** Current data · **Status:** Supporting

**Why:** Timestamps can describe successful completion time.

### AD-P06 — Which refunds, late captures, or orphan payment records need reconciliation?

**Decision:** Not selected now.
**Priority:** High · **Data:** Partial · **Status:** Planned

**Why:** Refunds, late captures, and orphan records can create money-integrity risk, but complete detection and ownership are not yet governed.

## E. Payouts and bank verification

### AD-F01 — Which payout requests await processing?

**Decision:** Selected for the current dashboard.
**Priority:** High · **Data:** Current data · **Status:** Selected

**Why:** Shows outstanding seller-money obligations. Keep currencies separate; the oldest-first order still needs backend support.

**Dashboard item:** **Payouts Awaiting Processing** — Action queue.

### AD-F02 — Which payouts are currently being processed?

**Decision:** Not selected for the current dashboard.
**Priority:** Medium · **Data:** Current data · **Status:** Supporting

**Why:** In-flight payout work belongs in the payout drill-down.

### AD-F03 — Which payouts failed, and why?

**Decision:** Selected for the current dashboard.
**Priority:** High · **Data:** Current data · **Status:** Selected

**Why:** Sends failed payouts to investigation and recovery. Show only safe reasons and actions to authorized administrators.

**Dashboard item:** **Failed Payouts** — Action queue.

### AD-F04 — How long does a successful payout normally take?

**Decision:** Not selected now.
**Priority:** Future · **Data:** Needs rule · **Status:** Planned

**Why:** Payout service-time target must be adopted before warning/overdue claims.

### AD-F05 — How much payout value was completed, by currency?

**Decision:** Not selected for the current dashboard.
**Priority:** Medium · **Data:** Current data · **Status:** Supporting

**Why:** Currency-separated payout throughput context.

### AD-F06 — Which payout bank accounts await verification?

**Decision:** Selected for the current dashboard.
**Priority:** High · **Data:** Current data · **Status:** Selected

**Why:** Shows bank-verification work that blocks safe payouts. Display only safe bank details to authorized administrators.

**Dashboard item:** **Bank Accounts Awaiting Verification** — Action queue.

### AD-F07 — Which bank accounts were rejected or disabled?

**Decision:** Not selected for the current dashboard.
**Priority:** Medium · **Data:** Current data · **Status:** Supporting

**Why:** Rejection/disable reasons can reveal recurring verification issues. Keep it for investigation rather than the main dashboard.

### AD-F08 — Does every wallet balance reconcile with its ledger?

**Decision:** Selected for the current dashboard.
**Priority:** High · **Data:** Current data · **Status:** Selected

**Why:** Shows a warning and mismatch queue only when wallet and ledger totals disagree. A passing operational check is not accounting certification.

**Dashboard item:** **Wallet–Ledger Reconciliation** — Conditional status.

## F. Users, stores, safety, and support

### AD-U01 — How many new users joined Angkoro?

**Decision:** Not selected for the current dashboard.
**Priority:** Low · **Data:** Current data · **Status:** Supporting

**Why:** User growth is context, not platform paid health.

### AD-U02 — How are users distributed across active, unverified, suspended, banned, or merged states?

**Decision:** Not selected for the current dashboard.
**Priority:** Medium · **Data:** Current data · **Status:** Supporting

**Why:** Supports account-health navigation. Keep it for investigation rather than the main dashboard.

### AD-U03 — Which users have remained unverified longer than the adopted limit?

**Decision:** Not selected now.
**Priority:** Future · **Data:** Needs rule · **Status:** Planned

**Why:** Requires a verification-age threshold and owner action.

### AD-U04 — Which users or stores are suspended or banned?

**Decision:** Not selected for the current dashboard.
**Priority:** Medium · **Data:** Current data · **Status:** Supporting

**Why:** Gives administrators visibility into safety enforcement and affected accounts.

### AD-U05 — Which reports, appeals, or support cases await review?

**Decision:** Not selected now.
**Priority:** Future · **Data:** Gap · **Status:** Planned

**Why:** A full admin surface needs accountable case handling, but no authoritative support/report workflow currently exists.

### AD-U06 — Can every sensitive admin action be traced to admin, time, reason, and result?

**Decision:** Not selected now.
**Priority:** High · **Data:** Partial · **Status:** Planned

**Why:** Administrator accountability is mandatory, but only some sensitive actions currently preserve complete actor, time, reason, and result evidence.

## G. Onboarding, Telegram, plans, and features

### AD-O01 — Which store-onboarding operations failed?

**Decision:** Not selected for the current dashboard.
**Priority:** Medium · **Data:** Current data · **Status:** Conditional alert

**Why:** Onboarding failures are rare and transient — a webhook timeout or duplicate slug, fixed once, gone. Show as a conditional alert when a failure occurs rather than occupying permanent overview space. Do not label merely old or slow operations as failed.

### AD-O02 — Which onboarding operations stopped progressing?

**Decision:** Not selected now.
**Priority:** Future · **Data:** Needs rule · **Status:** Planned

**Why:** Silent onboarding stalls matter, but each stage needs an adopted age limit and escalation owner.

### AD-O03 — At which onboarding step do businesses stop most often?

**Decision:** Not selected now.
**Priority:** Future · **Data:** Gap · **Status:** Planned

**Why:** Reliable step conversion needs immutable transition events.

### AD-O04 — How long does successful onboarding normally take?

**Decision:** Not selected for the current dashboard.
**Priority:** Low · **Data:** Partial · **Status:** Supporting

**Why:** Current timestamps can describe only limited duration behavior.

### AD-O05 — Which requested or connected Telegram setups are unhealthy?

**Decision:** Not selected for the current dashboard.
**Priority:** Medium · **Data:** Current data · **Status:** Supporting

**Why:** Identifies requested or connected channel setups that are not healthy.

### AD-O06 — Are active plans mapped to the intended features and limits?

**Decision:** Selected for the current dashboard.
**Priority:** High · **Data:** Current data · **Status:** Selected

**Why:** Shows a warning only when paid access and configured entitlements disagree. Compare against the adopted plan catalog; do not infer intended limits from usage.

**Dashboard item:** **Plan Entitlement Integrity** — Conditional status.

### AD-O07 — Which stores are reaching or exceeding plan limits?

**Decision:** Not selected now.
**Priority:** Future · **Data:** Partial · **Status:** Planned

**Why:** Needs governed current-usage measures and intervention rules.

## H. Platform reliability and data quality

### AD-R01 — Is the Angkoro API available, fast enough, and within an acceptable error rate?

**Decision:** Not selected now.
**Priority:** High · **Data:** Partial · **Status:** Planned

**Why:** Platform availability is essential; a liveness probe and optional Sentry exist, but no governed SLA, latency series, or error-rate aggregate exists.

### AD-R02 — Which background jobs are failing or stuck?

**Decision:** Not selected now.
**Priority:** High · **Data:** Partial · **Status:** Planned

**Why:** Durable jobs run critical workflows, but Angkoro has no administrator queue-health aggregate or recovery surface.

### AD-R03 — Are database, Redis, server, or disk resources near capacity?

**Decision:** Not selected now.
**Priority:** High · **Data:** Gap · **Status:** Planned

**Why:** Database, Redis, server, memory, and disk saturation can cause outages; these signals require external infrastructure telemetry.

### AD-R04 — Did the latest database backup complete successfully?

**Decision:** Not selected now.
**Priority:** High · **Data:** Gap · **Status:** Planned

**Why:** Recovery depends on verified backups, but backup execution evidence belongs to deployment infrastructure and is not currently integrated.

### AD-R05 — Which payment webhooks failed or could not be matched?

**Decision:** Not selected now.
**Priority:** High · **Data:** Partial · **Status:** Planned

**Why:** Webhook failures can block payment and payout state, and callback records exist, but an administrator recovery queue is not yet governed.

### AD-R06 — Is dashboard data current, complete, and based on the full population?

**Decision:** Selected for the current dashboard.
**Priority:** High · **Data:** Current data · **Status:** Selected

**Why:** Shows when dashboard data is stale, partial, missing, or incomplete. Missing or failed data is `Unknown`, never zero or healthy.

**Dashboard item:** **Dashboard Data Trust** — Conditional status.

### AD-R07 — Do independently recomputed dashboard totals reconcile with authoritative source records and financial ledgers?

**Decision:** Selected for the current dashboard.
**Priority:** High · **Data:** Current data · **Status:** Selected

**Why:** Checks whether an independent calculation agrees with the dashboard and its financial sources. If the check is missing, stale, or fails, show `Unknown` or `Not connected` instead of Passed. This is broader than Wallet–Ledger Reconciliation.

**Dashboard item:** **Source and Financial Reconciliation** — Conditional status.

## I. Security, abuse, and incidents

### AD-X01 — Is the public website or API currently receiving abnormal or attack traffic?

**Decision:** Not selected now.
**Priority:** High · **Data:** Gap · **Status:** Planned

**Why:** Attack and abnormal-traffic visibility is required for platform protection, but current throttling and lockout controls do not provide a durable request baseline or WAF feed.

### AD-X02 — Which authentication endpoints and IP addresses triggered repeated failures or lockouts?

**Decision:** Not selected now.
**Priority:** High · **Data:** Partial · **Status:** Planned

**Why:** Repeated authentication failures and lockouts can indicate credential attacks or broken clients, but temporary Redis counters and logs do not provide a durable administrator queue.

### AD-X03 — Which active sessions show an unusual IP address or user-agent change that needs review?

**Decision:** Not selected now.
**Priority:** High · **Data:** Partial · **Status:** Planned

**Why:** Session IP, user-agent, channel, and activity evidence can support investigation, but Angkoro lacks governed anomaly rules, safe platform-admin delivery, and a response workflow.

### AD-X04 — Which WAF or edge-security alerts require investigation?

**Decision:** Not selected now.
**Priority:** High · **Data:** Gap · **Status:** Planned

**Why:** Domain attacks should be blocked and reported at the edge, but no WAF or edge-security alert feed is integrated.

### AD-X05 — Which users, stores, payments, or payouts show unusual behavior that needs investigation?

**Decision:** Not selected now.
**Priority:** High · **Data:** Needs rule · **Status:** Planned

**Why:** Cross-platform abuse and money-movement anomalies require review, but baselines, severity, ownership, and false-positive controls are unresolved.

### AD-X06 — Which security incidents remain unresolved?

**Decision:** Not selected now.
**Priority:** High · **Data:** Gap · **Status:** Planned

**Why:** Security alerts need severity, ownership, status, and resolution tracking, but no authoritative incident workflow exists.

## Final dashboard items

1. **AD-G02 — Active Paid Stores** — Primary KPI
2. **AD-S01 — Subscription Collections** — Primary KPI
3. **AD-C01 — Platform Paid Orders** — Primary KPI
4. **AD-C02 — Platform Paid Sales** — Primary KPI
5. **AD-F01 — Payouts Awaiting Processing** — Action queue
6. **AD-F03 — Failed Payouts** — Action queue
7. **AD-F06 — Bank Accounts Awaiting Verification** — Action queue
8. **AD-S07 — Renewals in Grace** — Action queue
9. **AD-F08 — Wallet–Ledger Reconciliation** — Conditional status
10. **AD-O06 — Plan Entitlement Integrity** — Conditional status
11. **AD-R06 — Dashboard Data Trust** — Conditional status
12. **AD-R07 — Source and Financial Reconciliation** — Conditional status

AD-O01 (Failed Onboarding) appears only as a conditional alert when an explicit failure occurs. AD-S03 and AD-G05 remain available on the Analytics page.

## Final decision

All 66 questions remain documented. The current dashboard includes only the approved items above; supporting, combined, separate-surface, and planned questions remain available here without crowding the dashboard.

For the approved content definitions, use [03_Dashboard_Content.md](03_Dashboard_Content.md).
