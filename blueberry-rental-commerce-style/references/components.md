# Blueberry Rental Commerce Components

## Top Banner

Use for the homepage first viewport.

- Full width: `390px`.
- Height around `458px`.
- Real riding/product image.
- Add upper/lower masks when text or tabs need readability.
- Carousel indicator: small rounded bars or dots centered near the bottom.

## Top Status / Header

- iOS-style status bar at 44px.
- Header title can sit at the center or be hidden over the hero.
- Right side may include mini program controls or compact actions.

## Primary Category Tabs

Examples:

- `推荐`
- `精选车型`
- `门店推荐`
- `骑行路书`

Rules:

- Use horizontal layout.
- Active tab is larger/bolder and darker.
- Inactive tabs are smaller and muted.
- Keep tabs close to top hero or section title.

## Recommendation Entry Tiles

Use for quick entries like `口令码`, `Ebike`, `公路车`, `折叠车`, `儿童车`, `骑行服装`.

- Size around `132 × 60px`.
- Horizontal scroll with 4px gap.
- Soft card backgrounds with subtle image/product illustration on the right.
- Title: 14px semibold.
- Subtitle: 12px muted.
- Optional arrow at bottom-right.
- Drop shadow: subtle, around `0 2px 4px rgba(17,17,17,.04)`.

## Product Card

Use for rental/sale products.

Required structure:

- White rounded card.
- Large product image top area.
- Optional product color swatches near bottom of image.
- Product title.
- One-line descriptor.
- Price group with rental price and optional hourly price.
- Optional original sale price.
- Black capsule CTA: `选TA`, `去租车`, `立即预约`, or equivalent.

Sizing:

- Card: `361-366px × 342px`.
- Radius: `12px`.
- Image: `359 × 225px`.
- CTA: `89 × 36px`, radius `18px`.

## Product Rail Card

Use for horizontal product browsing.

- Card width about `329px`.
- Height about `446px`.
- Image area about `278px`.
- Footer price row around `60px`.
- Card content should be readable when partially clipped in horizontal scroll.

## Vehicle Detail Price Strip

Use below a vehicle detail hero image.

- Full width relative to the 390px canvas.
- Height about `88-96px`.
- Background: dark blue-black, e.g. `#172033` to `#40577B`.
- Top label: brand/source, 11px white.
- Main price row: day price and hour price, 14-18px, separated by a slim divider.
- Support text: original price or new-bike price, 11px, low-contrast white.
- Do not place this strip inside the vehicle image area.
- This strip is mandatory on vehicle detail pages when rental pricing exists.

## Marketplace Product Detail Card

Use below the product hero when the page follows a marketplace transaction structure.

- White full-width card.
- Price appears first and largest.
- Original price/discount tags sit inline with price.
- Product title follows, 20px or less, 1-3 lines.
- Source/official delivery row below title.
- No rounded floating card effect; it should feel like a content block.

## Marketplace Protection Strip

- Light mint or blue-tinted strip.
- One-line trust claims.
- Compact text around 13px.
- Place immediately below the product info card.

## Marketplace Attribute Strip

- White row with 4-5 equal columns.
- Value top, label bottom.
- Thin separators.
- Use for price, publish date, fit, model year, color, material, store distance, or availability.

## Vehicle Detail Selection Card

Use after the vehicle title.

- White card, radius about `12-16px`, padding `16px`.
- Color row should prefer vehicle thumbnail preview cards when multiple real SKU images exist. Use pure 26px circular swatches only as a fallback when vehicle-color thumbnails are unavailable.
- Thumbnail color cards should show the full vehicle, color name, stock state, and selected outline. Typical size: `76-86px × 58-68px`.
- Tapping a thumbnail color card should update the hero image, selected color name, size availability, and store availability copy.
- If the top hero already includes thumbnail images for color/model selection, do not repeat the same color cards again inside the selection card. In that case, the selection card should show only a compact selected-color summary plus size, stock, plan, and store availability.
- Option tiles such as handlebar/stem can use `62 × 40` rectangles with checker or solid fill.
- Size row uses equal buttons, about `64 × 38`, active item with outline/fill.
- Helper hint pill is small, dark blue, and placed below the size row.

If the production reservation flow selects rental dates/times after tapping the reservation CTA, do not show `日租` / `时租` as selectable plan cards on the detail page. Detail pages may show prices as information, but rental duration selection belongs in the calendar/date picker flow.

## Text Fit Rules

These rules are mandatory for Blueberry outputs:

- Never allow Chinese labels or body copy to break into awkward single-character lines, such as `骑 行`, `灵 活`, `门店自 提`, or vertical-looking `保 障`.
- Compact cards must either use shorter copy, smaller text, wider cards, or `white-space: nowrap` with ellipsis.
- Multi-benefit service rows should use chips or two short lines instead of one long sentence in a narrow container.
- A label such as `保障` should stay in one unbroken pill or fixed-width label. Do not let each character wrap onto separate lines.
- Rental plan descriptions in cards must fit within one or two natural lines. If the card is narrow, use short copy like `半日以上` and `短途灵活`.

## Vehicle Detail Parameter Card

Use for detailed specs.

- White card, radius about `12-16px`.
- Two-column layout.
- Label: 12px muted gray.
- Value: 13px dark text.
- Row spacing about `14-18px`.

## Fidelity Anti-Patterns

Avoid these because they reduce resemblance to the production Blueberry design:

- Product title or paragraph text overlaid on the bike image area.
- Price shown as a small badge beside the bike image instead of as a dedicated commerce row/strip.
- Large marketing typography inside product or detail pages.
- Nested cards inside cards.
- Heavy decorative gradients where the reference uses white or light gray.
- Generated SVG bikes as primary product imagery.
- Rebuilding product image backgrounds with ad hoc CSS when a composed PNG exists.

## Brand / Small Category Filter

Use vertical or horizontal filters depending on page layout.

Examples:

- `Blueberry`
- `小布`
- `Specialized`

Rules:

- Active item uses a soft rounded pill/background.
- Keep brand names compact and readable.

## Section Header

Examples:

- `好物推荐·租售随心选`
- `本周上新`
- `热卖Ebike`

Rules:

- Left aligned, strong black.
- Optional right action: `探索更多 ›`.
- If a section has secondary tabs, place tabs directly below the title.

## Liquid Glass Bottom Navigation

Use for persistent navigation.

- Width: `366px`, height: `64px`.
- Radius: `34px`.
- Position: 12px from left/right, above home indicator.
- Background: translucent white with blur.
- Active item: dark circular icon background or dark icon emphasis.
- Items typically: home, control/rental, profile.

## Bottom Sheet

Use for rider info, filters, or selection.

- White sheet over dim overlay.
- Max visible height can be around 80% of screen.
- Header height around 58px.
- Fixed bottom CTA area.
- List rows around 56px to 66px.

## Rider Info Row

Use in order flows.

- Row height around 66px.
- Left radio/check.
- Main name.
- Secondary masked ID.
- Right edit icon.
- Swipe delete reveals red delete area.
