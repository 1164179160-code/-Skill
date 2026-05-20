# Blueberry Fidelity Rules

Use these rules when the user asks to generate a page that should be almost indistinguishable from the Blueberry Figma style.

## Identity Lock

This style is a light cycling rental-commerce style.

It must look like:

- Blueberry riding / rental storefront.
- Premium bike rental and retail marketplace.
- Large clean product photography.
- White rounded commerce cards.
- Black capsule CTAs.
- Soft gray studio backgrounds.
- Translucent Liquid Glass bottom navigation.

It must not look like:

- ZD10 dark device controller.
- Smart lock page.
- Bluetooth hardware status page.
- Pixel LED editor.
- Dark neon dashboard.

## Page Skeletons

### Home / Discovery Page

Use this order:

1. iOS status bar.
2. Full-width hero/banner, `390 × 430-458`.
3. Top category tabs over or near hero:
   - `推荐`
   - `精选车型`
   - `门店推荐`
   - `骑行路书`
4. Horizontal recommendation entries:
   - each about `132 × 60`
   - 4px gap
   - title + subtitle + product/illustration on right
5. Section title:
   - e.g. `好物推荐·租售随心选`
   - right action `探索更多`
6. Secondary category tabs:
   - `租车`
   - `二手车`
   - `自研产品`
   - `甄选好物`
   - `友商合作`
7. Product card list or rail.
8. Liquid Glass bottom navigation.

### Product Card Feed

Use a vertical list of white cards:

- Card size: about `361 × 342`.
- Outer radius: `12`.
- Top image: about `359 × 225`.
- Text block starts around `x=13`, `y=238`.
- Product name: 20px rounded bold.
- Description: 12px gray.
- Footer row: 60px.
- Price number: 18-20px bold.
- Unit: 10-12px regular.
- CTA: black pill, `89 × 36`, radius `18`, right aligned.

### Vehicle List / Curated Goods Page

Use this when the page is a Blueberry vehicle list, rental mall list, or curated goods list such as `甄选好物`.

Reference structure:

1. iOS status bar.
2. Brand/title row:
   - Blueberry logo at left.
   - Mini program controls at right when needed.
3. Primary channel tabs:
   - `租车`
   - `二手车`
   - `自研产品`
   - `甄选好物`
   - `友商合作`
4. Filter chip row:
   - `类型`
   - `租赁价`
   - `排序`
   - 32px high rounded or glass-like pills.
5. Horizontal category shortcut row:
   - helmet, jersey, cycling shoes, water bottle, or bike-category entries.
   - Small white pills with image thumbnail and label.
6. Section header:
   - Strong title, e.g. `极限运动系列`.
   - Right action, e.g. `探索更多 ›`.
7. Vertical product card feed:
   - Large white card.
   - Top image area uses real PNG product/vehicle photography.
   - Color swatches below the image.
   - Product name and short descriptor.
   - Price row with day/hour price and black CTA.

Key differences from a detail page:

- The list page keeps controls above results; it should not start with a large hero banner unless it is the home/discovery page.
- Product cards are the main content unit. Do not turn the first product into a full detail hero.
- Filter and category rows are functional browsing controls, not decorative tags.
- When the product is non-bike gear, keep the same card structure but use the gear image as the visual anchor.

### Product Rail

Use a horizontal rail when showcasing multiple bikes:

- Card width: about `329`.
- Card height: about `446`.
- Image region: about `278`.
- Text block around `y=301`.
- Footer price row around `y=386`.
- Leave partial next card visible when possible.

### Vehicle Detail Page

Use this structure when the requested page is a transaction-oriented product detail page. If the user only asks to reference a marketplace app for the header, borrow only the header structure and keep the rest as Blueberry rental-commerce detail.

1. iOS status bar and simple top nav over a clean product hero.
2. Large product image area, about `390 × 400-430`.
   - Vehicle centered and fully visible.
   - Vehicle should be large enough to inspect; avoid tiny centered bike images.
   - Prefer transparent vehicle PNG directly on the page surface; do not show a visible image rectangle behind the bike.
   - No title, description, or price overlaps the vehicle image.
   - Add thumbnail strip and color/variant entry near the bottom of the hero.
3. White product information card.
   - Large price first.
   - Sale/original price and offer tags inline.
   - Product title below price, usually 1-3 lines.
   - Source/official delivery row below title.
4. Trust/protection strip.
   - Light mint/blue surface.
   - One-line service claims such as official supply, return policy, delivery support.
5. Attribute strip.
   - 4-5 equal columns.
   - Top value, bottom label.
6. Recent purchase / price trend module if commerce credibility is useful.
7. Fixed bottom action bar.
   - Left utility actions.
   - Secondary price/offer action.
   - Right strong buy/rent CTA.

Even when borrowing this marketplace structure, keep Blueberry visual language:

- Use Blueberry light gray page surface, white rounded cards, black primary CTA, compact commerce typography, and subdued shadows.
- Do not copy non-Blueberry accent colors such as bright cyan marketplace buttons.
- Do not copy oversized marketplace price typography if it makes the page feel off-brand; keep price prominent but controlled.
- Use the reference only for structure, not for color, icon, or brand tone.

Use the older parameter-heavy detail structure only when the page goal is equipment inspection or store reservation rather than marketplace transaction.

### Dewu-Like Header Only

When the user says the header should reference Dewu-like structure:

- Use a large product image area.
- Add product count text.
- Add thumbnail row.
- Add color/variant entry on the right.
- Then return to Blueberry detail structure: price/title card, rental plan card, color/size card, store card, parameter card, fixed black CTA.
- Do not add Dewu-like protection strip, attribute strip, price trend, cyan CTA, or oversized price unless the user explicitly asks for a full marketplace transaction page.

Avoid on detail pages:

- Overlaying product title or descriptive text on top of the vehicle image.
- Placing price as a small side badge beside the vehicle.
- Using dark decorative hero backgrounds that reduce product inspection.
- Making the first viewport feel like a marketing poster instead of a rental product detail.

### Order / Rider Sheet

Use a white bottom sheet:

- Width: `390`.
- Header height: `58`.
- Max visible height: up to `80%`.
- Add-rider button: about `358 × 46`.
- Rider row: `358 × 66`.
- Fixed bottom CTA area: `390 × 106`.
- Home indicator area: `34`.

## Exact Component Ratios

### Recommendation Entry

- Width: `132`.
- Height: `60`.
- Title: 14px semibold, `#0A0519`.
- Subtitle: 12px regular, `#999999`.
- Right image/illustration should overlap lightly.
- Use very soft drop shadow: `0 2px 4px rgba(17,17,17,.04)`.

### Product Image Area

- Use pale gray/white studio image background.
- Product should be centered and large.
- Add subtle shadow under bike tires.
- If multiple colors exist, show small circular swatches:
  - `12px` circles.
  - 8px to 20px spacing.
  - Selected swatch can be `16px`.

### Liquid Glass Bottom Nav

- Width: `366`.
- Height: `64`.
- Left/right inset: `12`.
- Radius: `34`.
- Background: translucent white plus blur.
- Active nav icon sits in a `52 × 52` circular dark emphasis.
- Do not add labels unless required by the current page pattern.

## Typography Lock

Prefer these exact roles:

- Product title: `Alimama FangYuanTi VF Bold-Square`, fallback rounded bold, `20px`, line-height `20px`, tracking `-0.4px`.
- Price number: `Alimama FangYuanTi VF Bold`, `18px`.
- CTA: `PingFang SC Semibold`, `14px`, line-height `22px`.
- Body: `PingFang SC Regular`, `12px`, line-height `18px`, `#666`.
- Metadata: `PingFang SC Regular`, `10px`, line-height `14px`, `#879099`.

## Color Lock

Use the palette without drifting:

- Main black: `#0A0519`.
- Body gray: `#666666`.
- Placeholder gray: `#879099`.
- Secondary gray: `#999999`.
- Page light gray: `#F5F6F7`.
- Card white: `#FFFFFF`.
- Home indicator black: `#111111`.

Avoid:

- ZD10 dark gray backgrounds: `#19191A`, `#232325`, `#262628`.
- ZD10 red accent `#FF3B3B`.
- Blue/purple gradients as the dominant treatment.

## Common Blueberry Screens

When asked to create a new Blueberry page, choose the closest screen type:

- Marketplace home: hero + recommendation entries + product cards.
- Product category page: category tabs + filters + product list.
- Product detail: large product photo + color swatches + rental price + CTA.
- Order confirmation: selected product + rider info + price summary + fixed payment CTA.
- Rider management: bottom sheet/list rows with radio and edit.
- Payment/deposit confirmation: clean white confirmation state, not a dark modal.

## Quality Checklist

Before finishing, check:

- Does it look light, white, and product-photographic?
- Does the primary action use a black capsule button?
- Is there a 390px mobile canvas?
- Are cards rounded white with subtle shadows?
- Are prices clearly visible and compact?
- Is the bottom nav glassy rather than flat?
- Are there no ZD10 dark hardware-control elements?

## High-Fidelity Self Review

Use this stricter review before delivering a Blueberry page:

- Page type: Does the layout match the closest production skeleton instead of a generic marketplace pattern?
- Image behavior: Are product images complete, clean, and inspection-friendly? Are they PNG assets rather than rough CSS reconstructions where a composite PNG exists?
- Information hierarchy: Is the strongest business decision visible in the correct place, such as a detail-page price strip or product-card footer?
- Density: Are spacing, font sizes, and card heights compact like commerce UI, not loose like a landing page?
- Component fidelity: Do controls look like production form controls/tabs/cards, not decorative concept components?
- CTA placement: Is the primary action where users expect it: card footer, detail fixed bottom bar, or sheet bottom area?
- Restraint: Remove any decorative treatment that is not visible in the reference style.
