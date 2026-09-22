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

## Typography

Poppins is embedded in the finished site under the SIL Open Font License.

<details>
<summary>Poppins copyright and license</summary>

```text
Copyright 2020 The Poppins Project Authors (https://github.com/itfoundry/Poppins)

This Font Software is licensed under the SIL Open Font License, Version 1.1.
This license is copied below, and is also available with a FAQ at:
http://scripts.sil.org/OFL


-----------------------------------------------------------
SIL OPEN FONT LICENSE Version 1.1 - 26 February 2007
-----------------------------------------------------------

PREAMBLE
The goals of the Open Font License (OFL) are to stimulate worldwide
development of collaborative font projects, to support the font creation
efforts of academic and linguistic communities, and to provide a free and
open framework in which fonts may be shared and improved in partnership
with others.

The OFL allows the licensed fonts to be used, studied, modified and
redistributed freely as long as they are not sold by themselves. The
fonts, including any derivative works, can be bundled, embedded, 
redistributed and/or sold with any software provided that any reserved
names are not used by derivative works. The fonts and derivatives,
however, cannot be released under any other type of license. The
requirement for fonts to remain under this license does not apply
to any document created using the fonts or their derivatives.

DEFINITIONS
"Font Software" refers to the set of files released by the Copyright
Holder(s) under this license and clearly marked as such. This may
include source files, build scripts and documentation.

"Reserved Font Name" refers to any names specified as such after the
copyright statement(s).

"Original Version" refers to the collection of Font Software components as
distributed by the Copyright Holder(s).

"Modified Version" refers to any derivative made by adding to, deleting,
or substituting -- in part or in whole -- any of the components of the
Original Version, by changing formats or by porting the Font Software to a
new environment.

"Author" refers to any designer, engineer, programmer, technical
writer or other person who contributed to the Font Software.

PERMISSION & CONDITIONS
Permission is hereby granted, free of charge, to any person obtaining
a copy of the Font Software, to use, study, copy, merge, embed, modify,
redistribute, and sell modified and unmodified copies of the Font
Software, subject to the following conditions:

1) Neither the Font Software nor any of its individual components,
in Original or Modified Versions, may be sold by itself.

2) Original or Modified Versions of the Font Software may be bundled,
redistributed and/or sold with any software, provided that each copy
contains the above copyright notice and this license. These can be
included either as stand-alone text files, human-readable headers or
in the appropriate machine-readable metadata fields within text or
binary files as long as those fields can be easily viewed by the user.

3) No Modified Version of the Font Software may use the Reserved Font
Name(s) unless explicit written permission is granted by the corresponding
Copyright Holder. This restriction only applies to the primary font name as
presented to the users.

4) The name(s) of the Copyright Holder(s) or the Author(s) of the Font
Software shall not be used to promote, endorse or advertise any
Modified Version, except to acknowledge the contribution(s) of the
Copyright Holder(s) and the Author(s) or with their explicit written
permission.

5) The Font Software, modified or unmodified, in part or in whole,
must be distributed entirely under this license, and must not be
distributed under any other license. The requirement for fonts to
remain under this license does not apply to any document created
using the Font Software.

TERMINATION
This license becomes null and void if any of the above conditions are
not met.

DISCLAIMER
THE FONT SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO ANY WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT
OF COPYRIGHT, PATENT, TRADEMARK, OR OTHER RIGHT. IN NO EVENT SHALL THE
COPYRIGHT HOLDER BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY,
INCLUDING ANY GENERAL, SPECIAL, INDIRECT, INCIDENTAL, OR CONSEQUENTIAL
DAMAGES, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING
FROM, OUT OF THE USE OR INABILITY TO USE THE FONT SOFTWARE OR FROM
OTHER DEALINGS IN THE FONT SOFTWARE.
```

</details>
