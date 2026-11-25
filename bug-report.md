# Bug Report — Toolshop Web Store

| | |
|---|---|
| **Application** | Toolshop (bug build) — https://with-bugs.practicesoftwaretesting.com |
| **Environment** | Google Chrome · Desktop (1456px) · guest user |
| **Tester** | Ahmed Mofrh Fahmy |

> Portfolio sample on a public practice site — not a client project.

## Summary

| ID | Issue | Severity |
|---|---|---|
| BUG-01 | Clearing the search with "X" empties the product grid | 🔴 High |
| BUG-02 | Quantity "+" and "−" buttons do not change the quantity | 🔴 High |
| BUG-03 | Cart line total shows $00.00 | 🔴 High |
| BUG-04 | Error message appears even though the item was added | 🟠 Medium |
| BUG-05 | Broken images: logo, search icon and one product thumbnail | 🟠 Medium |
| BUG-06 | "Add to cart" button overlaps "Add to favourites" | 🔵 Low |
| BUG-07 | Spelling mistakes in navigation and labels | 🔵 Low |
| OBS-01 | Price-range filter does not match the products shown | ⚪ Observation |

**Severity guide:** High = blocks or breaks a core journey (search, cart, checkout) · Medium = misleading or broken behaviour with a workaround · Low = cosmetic or text issues · Observation = possible issue needing confirmation of intended behaviour.

---

## BUG-01 — Clearing the search with "X" empties the product grid
**Severity:** High · **Area:** Home page product list  

**Steps**
1. Open the home page (9 products shown).
2. Type `pliers` in Search and click **Serch** (4 results shown).
3. Click the yellow **X** button to clear the search.
4. Wait 6+ seconds.

**Expected:** The full product list (9 products) is shown again.  
**Actual:** The product grid is completely blank — 0 products and no message. Only a full page reload restores the list.  
**Notes:** Reproduced 3/3 times in the first session; could not be reproduced on a later re-test, so it looks intermittent. Users who clear a search can be left on an empty shop.

## BUG-02 — Quantity "+" and "−" buttons do not change the quantity
**Severity:** High · **Area:** Product page (Combination Pliers)  

**Steps**
1. Open any product, e.g. Combination Pliers.
2. Click the **+** button next to the quantity.
3. Click the **−** button.

**Expected:** Quantity increases by 1 with "+" and decreases by 1 with "−" (minimum 1).  
**Actual:** Quantity stays unchanged after each click. It can only be changed by typing into the field.  
**Notes:** Checked with real mouse clicks. Blocks buying more than one item for most shoppers.

## BUG-03 — Cart line total shows $00.00
**Severity:** High · **Area:** Cart / checkout step 1  

**Steps**
1. Add Combination Pliers ($14.15) with quantity 2 to the cart.
2. Open the cart.

**Expected:** The line total shows $28.30 (2 × $14.15).  
**Actual:** The line total shows **$00.00**, while the cart total correctly shows $28.30.  
**Notes:** Inconsistent pricing at checkout damages trust and can cause abandoned carts.

## BUG-04 — Error message appears even though the item was added
**Severity:** Medium · **Area:** Product page → Add to cart  

**Steps**
1. Open Combination Pliers.
2. Click **Add to cart**.

**Expected:** A success confirmation such as "Product added to cart."  
**Actual:** A red toast says "Oeps, something went wrong.", yet the cart badge increases and the item is in the cart.  
**Notes:** Misleading feedback — users may add the item again and buy duplicates. The message is also not in English.

## BUG-05 — Broken images: logo, search icon and one product thumbnail
**Severity:** Medium · **Area:** Header, sidebar, product grid  

**Steps**
1. Open the home page.
2. Look at the top-left logo, the icon next to "Search", and the product thumbnails.

**Expected:** All images load.  
**Actual:** Three images fail to load: the logo and search icon (`broken.png`) and the product image `pliers05.jpeg`.  
**Notes:** Confirmed via the page's image list (`naturalWidth = 0`). Hurts credibility on the first screen.

## BUG-06 — "Add to cart" button overlaps "Add to favourites"
**Severity:** Low · **Area:** Product page  

**Steps**
1. Open Combination Pliers at desktop width (1456px).

**Expected:** Buttons sit side by side with clear spacing.  
**Actual:** The green "Add to cart" button covers the start of the yellow "Add to favourites" button.  
**Notes:** Visual/layout defect; risk of mis-clicks.

## BUG-07 — Spelling mistakes in navigation and labels
**Severity:** Low · **Area:** Header, sidebar, product page  

**Steps**
1. Open the home page and a product page.
2. Read the menu and section labels.

**Expected:** Correct English: Sort, Search, Contact, Related products.  
**Actual:** Shown as **Sorth**, **Serch** (button), **Contakt** and **Reltded products**.  
**Notes:** Quick fixes that make the shop look professional.

## OBS-01 — Price-range filter does not match the products shown
**Severity:** Observation · **Area:** Home page filters  

**Steps**
1. Open the home page and leave the price slider at its default (1–100).
2. Sort by Price (High – Low).

**Expected:** Either only products up to $100 are shown, or the slider defaults to the full range.  
**Actual:** Products priced $100.79–$125.23 are listed while the slider shows a 1–100 range.  
**Notes:** May be intended (filter not applied until the slider is moved), but it confuses users. Needs product-owner confirmation.
