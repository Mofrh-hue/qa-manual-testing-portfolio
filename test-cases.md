# Test Cases & Results — Toolshop Web Store

**20 test cases** for the core buying journey, executed in Chrome (desktop).
**Result: 12 passed · 7 failed · 1 needs review.** Every failed case links to the [bug report](bug-report.md).

> Portfolio sample on a public practice site — not a client project. Also available as [CSV](test-cases.csv) for import into a test-management tool.

| ID | Area | Test | Steps | Expected result | Result | Defect |
|---|---|---|---|---|---|---|
| TC-01 | Home | Home page loads product grid | Open home page | 9 products shown with name, image and price | ✅ Pass | |
| TC-02 | Home | All images load | Inspect logo, icons and thumbnails | All images render | ❌ Fail | [BUG-05](bug-report.md#bug-05--broken-images-logo-search-icon-and-one-product-thumbnail) |
| TC-03 | Home | Labels are spelled correctly | Read menu and sidebar labels | Sort, Search, Contact | ❌ Fail | [BUG-07](bug-report.md#bug-07--spelling-mistakes-in-navigation-and-labels) |
| TC-04 | Search | Search returns matching products | Search "pliers" | 4 pliers products shown | ✅ Pass | |
| TC-05 | Search | Search is case-insensitive | Search "HAMMER" | Same 6 results as "hammer" | ✅ Pass | |
| TC-06 | Search | No-results message | Search "xyzzy123" | "0 products found" message | ✅ Pass | |
| TC-07 | Search | Clear search restores list | Search, then click X | All products shown again | ❌ Fail | [BUG-01](bug-report.md#bug-01--clearing-the-search-with-x-empties-the-product-grid) |
| TC-08 | Sort | Name A–Z | Choose Name (A–Z) | Alphabetical order | ✅ Pass | |
| TC-09 | Sort | Name Z–A | Choose Name (Z–A) | Reverse alphabetical order | ✅ Pass | |
| TC-10 | Sort | Price low–high | Choose Price (Low–High) | Ascending prices | ✅ Pass | |
| TC-11 | Sort | Price high–low | Choose Price (High–Low) | Descending prices | ✅ Pass | |
| TC-12 | Filter | Price range respected | Default slider 1–100 | Only products ≤ $100 | ⚠️ Review | [OBS-01](bug-report.md#obs-01--price-range-filter-does-not-match-the-products-shown) |
| TC-13 | Product | Detail matches listing | Open Combination Pliers | Same name and price ($14.15) | ✅ Pass | |
| TC-14 | Product | Quantity + / − buttons | Click + then − | Quantity changes by 1 | ❌ Fail | [BUG-02](bug-report.md#bug-02--quantity--and--buttons-do-not-change-the-quantity) |
| TC-15 | Product | Quantity minimum | Type −3 in quantity | Value stays at minimum 1 | ✅ Pass | |
| TC-16 | Product | Add to cart feedback | Click Add to cart | Success message shown | ❌ Fail | [BUG-04](bug-report.md#bug-04--error-message-appears-even-though-the-item-was-added) |
| TC-17 | Product | Buttons laid out correctly | View action buttons | No overlap | ❌ Fail | [BUG-06](bug-report.md#bug-06--add-to-cart-button-overlaps-add-to-favourites) |
| TC-18 | Cart | Cart badge updates | Add item, check header | Badge shows item count | ✅ Pass | |
| TC-19 | Cart | Line total correct | Qty 2 × $14.15 | Line total $28.30 | ❌ Fail | [BUG-03](bug-report.md#bug-03--cart-line-total-shows-0000) |
| TC-20 | Cart | Cart total correct | Qty 2 × $14.15 | Cart total $28.30 | ✅ Pass | |
