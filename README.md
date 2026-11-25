# Manual QA Testing Portfolio

A complete manual testing package for a web shop: **test plan → test cases → bug report**, the way I'd deliver it to a client before a release.

> **About this sample:** this is portfolio work, not a client project. The application under test is **[Toolshop (bug build)](https://with-bugs.practicesoftwaretesting.com)**, a public web shop deliberately seeded with defects for QA practice. Every finding was reproduced in Chrome (desktop).

## Results at a glance

| | |
|---|---|
| Test cases executed | **20** |
| Passed / Failed / Needs review | **12 / 7 / 1** |
| Issues reported | **8** — 3 High, 2 Medium, 2 Low, 1 Observation |

The three **High** issues block the core buying journey:

1. Clearing a search with "X" empties the whole shop until the page is reloaded
2. The quantity + / − buttons don't change the quantity
3. The cart shows a `$00.00` line total while the cart total is correct

## Documents

| Document | What it contains |
|---|---|
| [Test plan](test-plan.md) | Objective, scope, approach, environment, entry/exit criteria, risks |
| [Test cases](test-cases.md) | 20 test cases with steps, expected results and Pass/Fail ([CSV version](test-cases.csv)) |
| [Bug report](bug-report.md) | 8 issues with severity, steps to reproduce, expected vs actual |

## Automated follow-up

The four most important defects are also automated as regression tests in **[playwright-ui-api-tests](https://github.com/Mofrh-hue/playwright-ui-api-tests)** (`tests/known-bugs`), so they stay visible in CI until fixed.

## How I work

- **Reproduce before reporting** — each defect was confirmed with real clicks or by inspecting the page, never guessed.
- **Write for the developer** — exact steps, expected vs actual, and the area affected, so a bug can be fixed without a follow-up question.
- **Severity by user impact** — anything that blocks search, cart or checkout is High; misleading behaviour is Medium; cosmetic issues are Low; unclear intent is an Observation for the product owner.

---

Author: **Ahmed Mofrh Fahmy** — QA Test Lead · [GitHub profile](https://github.com/Mofrh-hue)
