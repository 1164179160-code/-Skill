# Blueberry Page Style Library

Use this file to choose the correct Blueberry page framework before selecting components or assets.

## Home / Discovery

Use when the page introduces Blueberry riding, promotes categories, or routes users into rental/shop flows.

Structure:

1. iOS status and Blueberry brand area.
2. Large photographic hero or product banner.
3. Primary discovery tabs.
4. Horizontal quick entries.
5. Product recommendation section.
6. Product card rail or vertical product feed.
7. Liquid Glass bottom navigation.

Priority:

- First viewport should show Blueberry identity and a real product/riding visual.
- Discovery modules should lead to concrete categories, not generic marketing blocks.

Avoid:

- Desktop-like dashboards.
- Abstract hero illustrations.
- Too many cards before the first product.

## Vehicle List / Rental Mall

Use when the user browses vehicles by brand, model, type, price, size, or store availability.

Structure:

1. Status/header and Blueberry brand row.
2. Channel tabs such as `租车`, `二手车`, `自研产品`, `甄选好物`, `友商合作`.
3. Filter chips for type, rental price, brand, sort, store, or stock.
4. Optional horizontal category shortcut row.
5. Section title and right exploration action.
6. Vertical product cards.

Priority:

- Controls must feel functional.
- Product cards must show a large real image, title, descriptor, day/hour price, availability, and CTA.
- The first product can be emphasized, but should not become a detail page.

Avoid:

- Hero text that delays browsing.
- SVG bikes when real SKU PNGs exist.

## Curated Goods / Accessories

Use for helmets, cycling clothes, shoes, bottles, bags, and other non-bike goods.

Structure:

1. Same channel and filter framework as the vehicle list.
2. Category shortcut row with small product thumbnails.
3. Product cards where the item image is the visual anchor.

Priority:

- Maintain Blueberry commerce density.
- Use product-specific images and clear category labels.

## Vehicle Detail - Reservation

Use when the business goal is renting a specific vehicle from a store.

Structure:

1. Clean product hero with full visible vehicle.
2. Thumbnail or color entry near the hero if needed.
3. Rental price strip or price/title card depending on the chosen detail structure.
4. Product title and official/source copy.
5. Selection/confirmation module for selected color, size, current store stock, and guidance.
6. Store module with distance, hours, location, and contact/map actions.
7. Parameter card for frame, brake, wheel, transmission, handlebar, size guidance, or battery-related specs.
8. Product introduction or policy.
9. Fixed bottom action bar with service/contact and `预约租赁` / `立即预约`.

Priority:

- The vehicle image must be large enough to inspect.
- Do not duplicate rental duration selection if date/time is selected after CTA.
- Prevent wrong selection by making color, size, and store stock easy to read.

Avoid:

- Text over the vehicle image.
- Price as a small floating badge beside the bike.
- Tiny centered product images.
- Duplicate color cards if the hero already uses thumbnail selection.

## Vehicle Detail - Marketplace Header Reference

Use when the user asks for a Dewu-like top structure.

Borrow only:

- Large product image area.
- Product count text.
- Thumbnail row.
- Variant/color entry.

Keep Blueberry:

- Light gray page surface.
- White rounded cards.
- Black primary CTA.
- Compact price/title hierarchy.
- Blueberry rental logic below the header.

Avoid copying:

- Third-party accent colors.
- Oversized non-Blueberry price styling.
- Price trend or social proof modules unless requested.

## Reservation Calendar / Date Sheet

Use after tapping `预约` or `立即预约`.

Structure:

1. Bottom sheet or full calendar panel.
2. Selected product summary.
3. Calendar/date range selection.
4. Time slot or pickup/return time if needed.
5. Store stock and price refresh notice.
6. Confirm CTA.

Priority:

- Dates and time belong here, not as plan cards in the detail page.
- Disabled dates should be visible.
- Price and store inventory may refresh after date selection.

## Order Confirmation

Use after product, store, date, and rider information are chosen.

Structure:

1. Selected vehicle summary.
2. Rental time and pickup/return store.
3. Rider information.
4. Price breakdown, deposit, coupon, and policy.
5. Agreement/notice.
6. Fixed payment CTA.

Priority:

- Make editable fields obvious.
- Separate cost, deposit, and refundable/non-refundable policy.

## Rider Info Sheet

Use as a bottom sheet or page for selecting/editing rider identity.

Structure:

1. Sheet title and close action.
2. Add rider action.
3. Rider list rows with selected state, masked ID, edit action.
4. Fixed confirm CTA.

Priority:

- Keep rows dense and easy to scan.
- Support selected, editing, missing info, and verification states.

## Payment / Deposit

Use when the user is about to pay rental fee, deposit, or reservation hold.

Structure:

1. Order summary.
2. Amount and deposit distinction.
3. Payment method.
4. Policy or refund note.
5. Fixed pay CTA.
6. Success/failure feedback.

Priority:

- Price should be unambiguous.
- Avoid visual noise around payment decision.

## Store Module

Use on detail, order, or map-adjacent pages.

Structure:

- Store name.
- Distance.
- Business hours.
- Address.
- Available stock by selected variant.
- Map/navigation and call actions.

Priority:

- Store stock must update when variant changes.
- Location actions should be icon buttons with clear affordance.

