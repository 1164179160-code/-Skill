# High-Fidelity Generation Guide

Use this guide whenever the user asks for a Blueberry-style page and expects it to be close to the real product design.

## Generation Order

1. Pick the page type:
   - marketplace home
   - category/list page
   - vehicle detail page
   - order confirmation
   - rider info sheet
   - payment/deposit page
   - store/module page
2. Use the exact page skeleton from `blueberry-fidelity.md`.
3. Choose image assets in this order:
   - For large detail hero areas: use `assets/images/sku-clean/` directly, enlarged, with no separate white/image block.
   - For product cards and recommendation cards: use `assets/images/composite/` for finished product image regions.
   - For captured Blueberry references: use `assets/images/real-*.png`, `card-*.png`, `image-area-*.png`, `cover-*.png`.
   - SVG only for small fallback placeholders.
4. Build the page with production density:
   - compact text
   - small radii
   - white cards
   - restrained shadows
   - clear commerce rows
5. Run the high-fidelity self review in `blueberry-fidelity.md`.

## Page-Type Rules

### Marketplace Home

Use a large visual hero and discovery modules. This page can feel more promotional, but still needs commerce density below the hero.

Required:

- full-width visual hero
- horizontal quick entries
- product cards or product rail
- Liquid Glass bottom navigation

Avoid:

- starting with a plain filter panel
- using SVG bikes as hero imagery

### Category / Mall List

This is a shopping workflow, not a marketing page.

Required:

- search/location/mode controls
- brand or scenario filter
- result filter chips
- product list with image, name, descriptor, price, availability, CTA

When the requested page matches the existing Blueberry vehicle list or `甄选好物` list, use the stricter `Vehicle List / Curated Goods Page` skeleton in `blueberry-fidelity.md`:

- brand/title row first
- primary channel tabs
- filter chip row
- horizontal small category shortcut pills
- section title with right action
- vertical product card feed

Avoid:

- too many unrelated modules before results
- large hero text that delays browsing

### Vehicle Detail

Choose detail structure by business goal.

For marketplace/transaction pages, use:

1. clean large product hero
2. thumbnail strip / color entry
3. white price + title product card
4. protection strip
5. attribute strip
6. recent purchase or price trend card
7. fixed bottom trading bar

Keep the Blueberry style while using this structure:

- Black primary CTA instead of third-party marketplace cyan buttons.
- White cards with 12-16px radius and restrained shadows.
- Light gray Blueberry page background.
- Product price can be prominent, but should not dominate with an unrelated marketplace tone.
- Utility actions should be simple and quiet.

If the user only references Dewu for the header:

- Apply Dewu-like structure only to the hero: large product image, thumbnail row, color/variant entry.
- Continue with Blueberry detail modules below the header.
- Do not introduce third-party marketplace modules such as trend charts or oversized price blocks unless requested.

For store reservation or equipment inspection pages, use:

1. white/pale image area
2. rental price strip
3. product title
4. selection card
5. parameter card
6. store card
7. product intro
8. fixed CTA bar

Avoid:

- title, description, or price over the vehicle image
- floating price badges
- decorative hero layouts
- large rounded concept cards
- selectable `日租` / `时租` cards when the production flow selects rental time in the reservation calendar after CTA tap
- narrow text containers that produce awkward Chinese single-character line breaks

### Order / Rider / Payment

These pages should feel quiet and operational.

Required:

- clear selected bike/order summary
- editable rows and bottom sheet patterns
- fixed bottom CTA
- no decorative hero

## Asset Rules

- Finished pages should use PNG assets wherever possible.
- Use `composite/` assets for card/rail image areas when available to avoid rough CSS shadows/backgrounds.
- Do not use `composite/` detail images when the design needs a transparent vehicle directly on the page surface.
- Use `sku-clean/` when the page needs custom layout around the vehicle, especially large detail heroes.
- Never place original `sku/` PNGs on gray backgrounds because they may show white blocks.
- Every vehicle must be fully visible: no cropped wheels, handlebar, saddle, basket, or rear rack.

## Typography And Spacing

- Product/detail titles: 18-20px for dense commerce pages; avoid 30px+ unless it is a true homepage hero.
- Body/metadata: 10-12px.
- Detail cards: 12-16px radius, not oversized.
- Feed product cards: around 361-366px wide, 342px high.
- Detail page content inset: around 24px in online-style detail screens.
- Marketplace/list pages: 12px content inset.

## Final Self-Check

Before delivering, compare against the production reference:

- Is the page immediately recognizable as Blueberry?
- Did the layout reuse the correct production skeleton?
- Are the image assets clean PNGs, not rough approximations?
- Is pricing in the correct component for this page type?
- Are controls functional-looking rather than decorative?
- Did any ZD10 dark hardware style leak in?
- Did any Chinese copy split into unnatural single-character line breaks?
- If the flow uses a calendar after `预约`, did the detail page avoid duplicating rental-duration selection?
