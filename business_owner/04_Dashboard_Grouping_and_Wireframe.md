# 4. Business-Owner Dashboard Grouping and Wireframe

**Purpose:** Show the dashboard order and the simplest fitting display for each approved item. This is a proposed layout, not a completed interface.

## Dashboard groups

| Group | Approved items | Main question |
|---|---|---|
| Business health | Paid Sales; Paid Orders | Is the store generating valid paid business? |
| Needs attention | Orders Need Decision; Fulfillment Backlog; Inventory Attention | What should the seller act on now? |
| Supporting | Average Paid Order Value; Top Products | What explains the business-health result? |
| Conditional | Store Readiness | Is setup blocking the store? |

## Simple wireframe

```text
+------------------------------------------------------------------+
| BUSINESS OVERVIEW       Period | Currency | Last updated          |
+------------------------------------------------------------------+
| Paid Sales                       | Paid Orders                    |
| [USD and KHR shown separately]   | [count]                        |
+------------------------------------------------------------------+
| NEEDS ATTENTION                                                  |
| Orders Need Decision | Fulfillment Backlog | Inventory Attention |
+------------------------------------------------------------------+
| Average Paid Order Value         | Top Products                   |
| [small supporting card]          | [ranked list]                  |
+------------------------------------------------------------------+
| Store Readiness appears here only when setup needs attention.    |
+------------------------------------------------------------------+
```

On mobile, show the same groups in this order: needs attention when work exists, business health, supporting content, and Store Readiness only when needed.

## Display guide

| ID | Dashboard item | Simple display |
|---|---|---|
| BO-S01 | Paid Sales | USD/KHR KPI card with previous-period comparison and small trend |
| BO-S02 | Paid Orders | Count card with previous-period comparison and small trend |
| BO-O01 | Orders Need Decision | Queue sorted by nearest decision deadline |
| BO-F01 | Fulfillment Backlog | Queue sorted by oldest accepted order |
| BO-I05 | Inventory Attention | Prioritized list: out of stock first, then low stock |
| BO-S04 | Average Paid Order Value | Small USD/KHR supporting card |
| BO-I01 | Top Products | Ranked horizontal bars or simple ranked list |
| BO-R01–R06 | Store Readiness | Conditional setup checklist |

## Important rules

- Keep USD and KHR separate.
- Show the selected period and when the data was last updated.
- Action queues open the related authorized order or inventory workflow.
- Show Store Readiness only when setup needs attention.
- Show missing or failed data as `Unknown` or `Not connected`, never as zero or healthy.
- Use `03_Dashboard_Content.md` for definitions and guardrails; do not repeat them here.
