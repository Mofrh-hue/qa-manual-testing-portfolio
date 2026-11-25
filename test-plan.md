# Test Plan — Toolshop Web Store (pre-release)

| | |
|---|---|
| **Application** | Toolshop (bug build) — https://with-bugs.practicesoftwaretesting.com |
| **Test type** | Functional · UI · Exploratory |
| **Effort** | 1 focused session |
| **Prepared by** | Ahmed Mofrh Fahmy |

> Portfolio sample on a public practice site — not a client project.

## 1. Objective

Confirm that a shopper can find a product, choose a quantity, add it to the cart and see correct prices — and report anything that blocks or confuses them before release.

## 2. In scope

- **Home page:** product grid, images, navigation labels
- **Search:** query, results, no-results message, clearing the search
- **Sorting** (name and price, both directions) and the **price-range filter**
- **Product page:** data matches the list, quantity controls, Add to cart, feedback messages
- **Cart:** line totals, cart total, cart badge

## 3. Out of scope

Account sign-in and registration · payment submission · performance/load and security testing · mobile devices (recommended as a next step).

## 4. Approach

- **Scripted checks** from the [test-case sheet](test-cases.md) for each in-scope area
- **Exploratory testing** around the buying journey to find edge cases
- **Confirm before reporting:** each defect verified with real clicks or by inspecting the page
- **Evidence:** exact steps, expected vs actual, and page data where useful

## 5. Environment

| Item | Detail |
|---|---|
| URL | with-bugs.practicesoftwaretesting.com |
| Browser | Google Chrome (desktop), 1456px viewport |
| Data | Public catalogue; guest (not signed in) |

## 6. Entry and exit criteria

| Criteria | Definition |
|---|---|
| **Entry** | Build is reachable and the product catalogue loads. |
| **Exit** | All planned test cases executed; every defect logged with severity; no open High defects for release sign-off. |

## 7. Risks

- Defects in search or cart directly cost sales — tested first.
- Single browser only; cross-browser coverage is recommended before launch.

## 8. Deliverables

- This test plan
- [Test cases](test-cases.md) with Pass/Fail results
- [Bug report](bug-report.md) with severity and reproduction steps
