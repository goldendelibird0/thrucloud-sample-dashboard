# BizInDash

**Data in. Insights out. Grow faster.**

An interactive inventory dashboard featuring **Harborline Business Supplies**, a fictional office, packaging and cleaning supplies company.

**[Open BizInDash](https://goldendelibird0.github.io/thrucloud-sample-dashboard/?view=1&tab=dashboard)** · **[Open the Google Sheet](https://docs.google.com/spreadsheets/d/1YYowE_I_Cz20txaiCMt6YhfIQAStdb-3h43yDRKPvno/edit)**

## Explore

- **Overview:** inventory value, 90-day turnover, low stock, out of stock, near expiry, expired stock, overstock and backorders; a prioritized action list; category, location and stock-history breakdowns.
- **Inventory:** product register and focused expiry, backorder, overstock and slow/non-moving reports. Select a product for its stock history and planning details.
- **Purchasing:** suggested purchases and outstanding supplier orders, including overdue deliveries.

Category and location filters apply across the dashboard. **Open sheet** sits beside **Refresh**. The dashboard reads all three Sheet tabs on opening and Refresh; failed or invalid updates retain the last valid data with an explanation.

## Demo data and definitions

The sample has 1,000 products, 15,586 movements and 96 open orders. All company details and records are fictional. The fixed snapshot is **September 11, 2026**, with 90 days of history beginning June 14. Sync time is separate from the snapshot date; this is not a rolling inventory system.

- **Available stock** = physical Quantity minus Quantity Reserved. Low/out-of-stock alerts use availability. Inventory value uses physical stock at cost.
- **Turnover** = cost of sales over the full 90 days divided by average daily inventory value over the same period. It is not annualized.
- **Near expiry** means 0–30 days from the snapshot; earlier dates are Expired. One date applies to all current units of a product. Expired units are flagged, not automatically removed.
- **Overstock** uses physical Quantity above Max Stock. The maximum is an illustrative planning input.
- **Backorders** count products with customer demand awaiting supply. Quantities stay in the product list, where their units are meaningful. Supplier purchase orders are separate.
- **Slow-moving** means no receipt or sale for 30–59 days; **Non-moving** means 60+ days. No activity in the available history is shown as 90+ days.
- **Suggested top-up** = target stock + backorders − available stock − incoming orders, floored at zero when replenishment is needed. Without recent sales or backorders, review demand first. Suggestions do not create orders.

## Editing the sample

Use the Sheet's owner account; public visitors have read-only access. Keep the three tab names and row 5 headers unchanged. Product IDs link the tabs. Quantity must reconcile to Opening Quantity + Receipts − Sales. The new inputs are **Quantity Reserved**, **Max Stock**, and **Backorder Quantity** in Inventory columns P:R. Reservations cannot exceed physical quantity; Max Stock must be at least Target Stock and Reorder Level; backorders cannot be negative. Stock status in both Inventory and Open orders recalculates from the master record.

**[Download the updated sample workbook](sample-data/harborline_inventory_demo.xlsx)** — a saved baseline matching this release. Later edits in Google Sheets do not automatically change the download.

This repository contains only the finished static site, saved fallback dataset and sample workbook. Editing projects, build scripts and internal runtime source remain outside this public repository. The existing GitHub Pages address is retained.
