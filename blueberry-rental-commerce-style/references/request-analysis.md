# Blueberry Request Analysis

Use this before generating, reviewing, or restructuring a Blueberry rental-commerce page. Keep it lightweight; the goal is to choose the right page framework, content hierarchy, assets, and interaction states.

## Infer First

- Page type: home/discovery, vehicle list, curated goods, vehicle detail, reservation, order confirmation, rider sheet, payment/deposit, store module, or review/PRD.
- Primary user: short-term renter, long-term renter, returning customer, price-sensitive user, performance bike user, store staff-assisted user, or browsing shopper.
- Entry point: home tab, search/filter, store recommendation, campaign, order, vehicle detail, or shared product link.
- Primary task: browse, compare, inspect, choose, reserve, pay, edit rider info, confirm store, or recover from an exception.
- Primary action: select product, choose variant, reserve, pay deposit, contact store, navigate, or retry.
- Secondary actions: collect/favorite, compare, switch store, view specs, view policies, contact service, open map, edit information.
- Required content: product image, product title, price, rental unit, stock, color, size, store distance, availability, service promise, specs, policy, CTA.
- Required states: loading, empty, error, selected, disabled, no stock, unavailable date, store closed, deposit required, success.
- Selection risk: wrong color, wrong size, wrong store, unavailable date, no current inventory, misunderstanding hourly/day price.
- Next step after this page: calendar, rider info, order confirmation, payment, store pickup, or product comparison.

## Clarify Only When Needed

Ask the user a question only when the missing answer would materially change page structure. Otherwise, make a reasonable assumption and state it briefly.

Examples:

- If the user asks for a vehicle detail page and does not mention date selection, assume dates are selected after tapping `预约/立即预约`.
- If no exact vehicle model is given, use the closest SKU PNG from `assets/images/sku-clean/`.
- If the page goal is browsing, prioritize filters and product cards. If the page goal is conversion, prioritize image inspection, price, stock, variant, store, and CTA.

## Translate Into Design Inputs

- Choose the closest page pattern from `page-style-library.md`.
- Use `blueberry-fidelity.md` for exact production-like skeleton and ratios.
- Use `components.md` for component anatomy and interaction expectations.
- Use `sku-vehicle-assets.md` for image choice and whether the image belongs in a hero, card, recommendation, or white display scene.
- Use `interaction-states.md` to cover the states that affect reservation or purchase completion.

## Required Rental-Commerce Questions

Before drawing, answer internally:

- What does the user need to understand in the first viewport?
- Is this a browsing page or a decision page?
- Is price informational or the main conversion driver?
- Where does the user choose rental time?
- Where does the user confirm color, size, and store stock?
- What can prevent successful reservation?
- Which module should be sticky or fixed?

