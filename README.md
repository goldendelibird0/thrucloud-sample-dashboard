# ThruCloud sample dashboard

An interactive inventory dashboard for **Harborline Business Supplies**, a fictional office, packaging and cleaning supplies company.

**[Open the dashboard](https://goldendelibird0.github.io/thrucloud-sample-dashboard/?view=1&tab=dashboard)** · **[Open the Google Sheet](https://docs.google.com/spreadsheets/d/1YYowE_I_Cz20txaiCMt6YhfIQAStdb-3h43yDRKPvno/edit)**

The Google Sheet powers the inventory, stock history, purchase orders and expiry worklists. The dashboard reads all three tabs on opening and when you select **Refresh**. The source link and last successful sync appear above the dashboard. If a refresh fails, the previous valid data stays visible with an explanation; the first load has a saved demo fallback.

## Editing the demo

- Edit the Sheet in its owner account. Public visitors have read-only access.
- Keep the three tab names and row 5 headers unchanged. Product IDs link the tabs.
- Edit product inputs, expiry dates, movement records and open orders. The dashboard recalculates values, stock status and action lists.
- Quantity must equal Opening Quantity + Receipts − Sales for each product. Update the stock quantity and matching movement together.
- This remains a fixed demonstration as of **September 11, 2026**, with history from June 14. Expiry and order deadlines use that snapshot date, not the sync time. It is not a rolling live inventory system.

The starting sample has 1,000 products, 15,586 movements and 96 open orders. Selected cleaning products have expiry dates; one date represents all current units of a product. Near expiration means 0–30 days from the snapshot, with expired stock shown separately. Needs attention counts a product once even when issues overlap. All company details and records are fictional.

**[Download the original sample workbook](sample-data/harborline_inventory_demo.xlsx)** — a saved baseline; later Google Sheet edits do not update this download.

## Publication files

This repository contains only the finished static site, the saved fallback dataset and the sample workbook. GitHub Pages serves the repository root on main. Editing projects, build scripts, internal documentation and runtime source files are kept outside this publication repository.
