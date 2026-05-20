# Blueberry Rental Commerce Style Rules

## Visual Keywords

Light premium, cycling rental, product photography, clean commerce, soft gray studio, rounded white cards, black capsule CTAs, horizontal discovery, Liquid Glass navigation.

## Canvas

- Mobile-first width: `390px`.
- Typical full-page height: `844px` or long scroll pages around `1896px`.
- Use a white or very light gray app background.
- Keep content inset mostly `12px`.
- Use full-width hero/banner at the top, around `390 × 458px` when it is the first visual anchor.

## Color

Base palette:

| Token | Value | Usage |
|---|---|---|
| `bg/page` | `#F5F6F7` | App background |
| `bg/card` | `#FFFFFF` | Product cards and sheets |
| `text/primary` | `#0A0519` | Main product names, prices, active icons |
| `text/body` | `#666666` | Product descriptions |
| `text/muted` | `#879099` | Supporting metadata |
| `text/subtle` | `#999999` | Secondary tile descriptions |
| `border/light` | `rgba(17,17,17,.06)` | Card separators |
| `cta/primary` | `#0A0519` | Primary capsule CTA |
| `white` | `#FFFFFF` | Cards and anti text |

## Typography

- Product title: Alimama FangYuanTi or rounded bold fallback, 20px, line-height 20px, tracking around `-0.4px`.
- Section title: 20px to 24px, bold, compact.
- Tab active: 20px or 24px, bold; inactive: 15px to 16px.
- Product description: PingFang SC Regular, 12px, line-height 18px.
- Price number: Alimama FangYuanTi Bold or rounded bold fallback, 18px to 20px.
- Price unit: PingFang SC Regular, 10px to 12px.
- CTA: PingFang SC Semibold, 14px, line-height 22px.

## Layout

- Product card width in feed: about `361px` to `366px`.
- Product card height: about `342px`.
- Card radius: `12px`.
- Product image area: about `359 × 225px`, with top corners rounded.
- Product info starts around 12px from the card left edge.
- Price/footer row height: about `60px`.
- Primary CTA inside card: `89 × 36px`, radius `18px`, right aligned.
- Category/recommendation entry size: about `132 × 60px`.
- Bottom navigation: `366 × 64px`, radius `34px`, 12px horizontal inset.

## Imagery

- Use real or realistic bike/product photography when possible.
- For vehicle detail hero areas, prefer cleaned transparent SKU PNGs from `assets/images/sku-clean/` enlarged directly on the page surface with no extra image background.
- Prefer polished composite product scenes in `assets/images/composite/` for finished product-card, marketplace list, and recommendation image regions.
- Prefer Figma-captured product assets in `assets/images/real-*.png`, `assets/images/card-*.png`, `assets/images/image-area-*.png`, and `assets/images/cover-*.png` when reproducing an existing Blueberry layout.
- Use cleaned transparent SKU assets in `assets/images/sku-clean/` when a component needs a custom composition. Original `assets/images/sku/` files are archival and often include white backgrounds.
- Use bundled SVG bike assets only as last-resort placeholders, never as the primary image when a real PNG exists.
- Product cards should have clean studio backgrounds: white, pale gray, or soft gradient.
- Bikes can float with subtle oval tire shadows.
- Do not over-darken product imagery.
- Keep color swatches on product cards as small 12px circles near the image bottom edge.

## Fidelity Discipline

- Start from the closest production page skeleton before adding any new idea.
- Match production hierarchy first, then polish. Structure beats decoration.
- Use smaller, denser product-commerce typography; avoid oversized hero marketing text on operational product pages.
- Keep cards simple: white fill, small radius, subtle shadow, compact controls.
- Product detail pages should feel like product inspection, not campaign advertising.
- Large vehicle hero images should not sit inside visible white rectangles or independent image blocks unless the reference explicitly shows that treatment.
- When a UI looks weaker than the online reference, reduce invention and copy the reference layout more directly.

## Shadows And Glass

- Cards use subtle shadows only, e.g. `0 2px 8px rgba(17,17,17,.04)`.
- Bottom nav uses translucent glass blur with a white fill and soft background blur.
- CTA uses solid black, not gradient.
