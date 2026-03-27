# Known Seeded Bugs — FOR QA LEAD EYES ONLY

> **This file should NOT be shared with the learner.** It lists the intentional flaws
> seeded into the feature specs for Module 4. Use this to verify the learner has found them.

## Bug 1 — Login: "Remember Me" contradiction
**Location:** `app/features/login.md`
**Flaw:** The spec says users stay logged in for 30 days, and "Remember Me" extends this to 90 days. But there is no mention of what happens if the user changes their password — are all sessions invalidated? The spec is silent on this, creating a security ambiguity.
**Severity:** Major
**Learner should raise:** An issue or question noting the spec gap.

## Bug 2 — Search: Empty search term
**Location:** `app/features/search.md`
**Flaw:** The spec does not define what happens if a user submits the search form with an empty search field. Should it show all products? An error? Nothing?
**Severity:** Minor
**Learner should raise:** A bug or spec-gap issue.

## Bug 3 — Cart: Guest "Add to Cart" inconsistency
**Location:** `app/features/cart.md`
**Flaw:** The spec says guests see an "Add to Cart" button that, when clicked, prompts login. But `app/features/login.md` says guests "cannot purchase" — the cart spec should say "cannot add to cart." Additionally, if a guest logs in after trying to add an item, should that item be added automatically? The spec doesn't say.
**Severity:** Major
**Learner should raise:** A bug report noting the inconsistency between specs.

## Bug 4 — Checkout: Postcode not validated
**Location:** `app/features/checkout.md`
**Flaw:** The checkout spec requires a postcode field but never states whether it's validated (format, length, country-specific rules). A user could enter "AAAA" as a postcode.
**Severity:** Minor
**Learner should raise:** A spec gap / bug issue.

## Stretch Bug 5 — Checkout: Amex CVV
**Location:** `app/features/checkout.md`
**Flaw:** The spec says "CVV is 3 digits (4 for Amex, but Amex is not supported)" — but it doesn't say what should happen if a user *tries* to enter an Amex card number. Should it be rejected at entry? Show an error? This is a UX gap.
**Severity:** Minor/Cosmetic
**Learner should raise:** Only advanced learners are likely to spot this.
