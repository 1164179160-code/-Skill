# Vehicle Assets Classification

This file classifies extracted vehicle-related assets from the Blueberry Figma file. Use it to choose the right image type for future page generation.

## Extraction Standard

When extracting vehicle assets from Figma, do not blindly export every node named `image`. Use this decision order:

1. **Export the most complete useful visual first**
   - For hero: export the complete banner/frame, not only the bike.
   - For product listing: export the complete product image area or full product card.
   - For custom composition: export a clean bike cutout only if it is visually complete and not clipped.

2. **Prefer parent frame when child export is broken**
   - Some rotated, masked, or transformed bike nodes export as `1 × 1`.
   - If a child bike node exports incorrectly, export its parent image area or product-card frame.
   - Example: if `image 513` exports as `1 × 1`, use `Frame 2036092145` or the card image area instead.

3. **Keep Figma context**
   - Record Figma node id.
   - Record original size.
   - Record parent context, e.g. `首页 / 更多好车 / Frame 2036092145`.
   - Record recommended usage category.

4. **Do not mix asset roles**
   - Hero images should not be used as product card thumbnails unless intentionally cropped.
   - Full product cards should not be used when text, price, or CTA need to be editable.
   - Cutouts should not be used without a studio background and wheel shadow.

## Asset Quality Criteria

### Keep

Keep an extracted image when it satisfies at least one of these:

- Contains a complete bike or rider-bike scene.
- Has enough surrounding background to work as a banner or card image.
- Is a complete product card from the original design.
- Is a clean product image area with bike, background, swatches, and shadows.
- Is a small vehicle/gear illustration designed for recommendation entries.

### Reject

Reject or avoid as primary assets:

- `1 × 1` exports.
- Shadows only, e.g. nodes named `投影`.
- Route/map thumbnails.
- Store photos unless making a store module.
- Payment/order page screenshots.
- Icon-only nodes.
- Cropped bike fragments without a complete vehicle silhouette.
- Duplicate instances with the same visual and same size.

## Naming Convention

Use semantic filenames so downstream generation can select assets without opening them.

### Cover / Poster

```text
cover-[subject]-[scene].png
```

Examples:

- `cover-rider-spring-road.png`
- `cover-bike-promo-wide.png`

### Complete Product Card

```text
card-[bike-type]-[index].png
```

Examples:

- `card-road-bike-01.png`
- `card-mtb-bike-02.png`

### Product Image Area

```text
image-area-[bike-type]-[index].png
```

Examples:

- `image-area-road-bike-01.png`
- `image-area-mtb-bike-02.png`

### Cutout / Recomposition

```text
cutout-[subject]-[index].png
```

Examples:

- `cutout-bike-display-01.png`
- `real-road-bike-cutout.png`

## Capture Matrix

| Figma Visual Type | Preferred Node To Export | Resulting Asset Type | Use In |
|---|---|---|---|
| Full top banner | `顶部banner` or complete image rectangle | Cover/poster | Homepage hero, category hero |
| Product card | Whole `Frame 2036092145` card | Complete card | Fast high-fidelity prototype |
| Product image area | Card top image rectangle/frame | Image area | Editable product card |
| Bike cutout | Bike image node, only if full and not broken | Cutout | Custom composition |
| Horizontal entry tile | Whole `推荐入口` item or its product image | Small entry asset | Quick entry rail |
| Detail product image | `车辆详情 / 商品图` parent | Detail image | Product detail/rental sheet |

## Classification Decision Tree

```text
Is it a full campaign/rider scene?
  -> Cover poster

Is it a complete product card with price and CTA?
  -> Complete product card

Is it only the top image area of a product card?
  -> Pure white / light studio display

Is it a clean complete bike with transparent/simple background?
  -> Cutout / custom composition

Is it small and designed for a horizontal shortcut tile?
  -> Recommendation entry asset

Is it a map, shadow, tiny icon, duplicate, or broken export?
  -> Do not use
```

## Export Checklist

Before adding an asset to the Skill:

- Open or preview it locally.
- Confirm the bike is visually complete.
- Confirm the exported dimensions are not `1 × 1`.
- Confirm the image is not only a shadow or background.
- Add it to `references/assets.md`.
- Add it to this classification file.
- If it should be reused by generated pages, mention its preferred use in `SKILL.md` or this file.
- Repackage `blueberry-rental-commerce-style.zip`.

## Summary

The Figma file contains many repeated vehicle nodes. Repeated instances are not all exported separately. The assets below are deduplicated representatives and are enough to cover the main visual patterns:

- Cover/poster hero
- Full product card
- Pure white or light-gray product display
- Transparent/cutout bike display
- Small recommendation-entry vehicle images
- Generated SVG fallback assets

## Best For Cover Posters

Use these when creating the first viewport, campaign banner, activity entry, or category hero.

| Asset | Figma Node | Size | Recommended Use |
|---|---:|---:|---|
| `assets/images/cover-rider-spring-road.png` | `0:1830` | `390 × 458` | 首页首屏大海报、活动页封面、骑行主题落地页 |
| `assets/images/cover-bike-promo-wide.png` | `0:9399` | `390 × 275` | 车型频道顶部 banner、短卡片海报、专题入口 |
| `assets/images/real-home-banner.png` | `0:1827` | `390 × 458` | 已合成完整首页 banner，适合直接贴入原型 |

Guidance:

- Prefer full poster assets for top hero.
- Do not crop too tightly; keep rider/bike motion and atmosphere.
- Use dark/blur overlays only if text readability is needed.

## Best For Complete Product Cards

Use these when you want maximum visual fidelity and do not need to recompose the card from smaller parts.

| Asset | Figma Node | Size | Recommended Use |
|---|---:|---:|---|
| `assets/images/card-road-bike-01.png` | `0:2358` | `363 × 342` | 完整商品卡、列表卡、租车推荐卡 |
| `assets/images/card-mtb-bike-02.png` | `0:2404` | `363 × 342` | 第二种完整商品卡、山地/进阶车型卡 |
| `assets/images/real-road-bike-card.png` | `0:2358` | `363 × 342` | 与 `card-road-bike-01.png` 同类，保留兼容旧引用 |
| `assets/images/real-product-card-02.png` | `0:2404` | `363 × 342` | 与 `card-mtb-bike-02.png` 同类，保留兼容旧引用 |

Guidance:

- Use full card assets when quickly producing a Figma-style mock.
- Use composable image-area assets instead if the product title, price, CTA, or stock status must be edited.

## Best For Pure White / Light Studio Product Display

Use these inside custom product cards when you need editable text/prices but realistic bike visuals.

| Asset | Figma Node | Size | Recommended Use |
|---|---:|---:|---|
| `assets/images/image-area-road-bike-01.png` | `0:2370` | `359 × 225` | 白/浅灰商品图区，适合标准商品卡图片区 |
| `assets/images/image-area-mtb-bike-02.png` | `0:2440` | `363 × 182` | 浅灰商品图区，适合紧凑商品卡或推荐位 |
| `assets/images/real-road-bike-image-area.png` | `0:2370` | `359 × 225` | 与 `image-area-road-bike-01.png` 同类，保留兼容旧引用 |
| `assets/images/real-product-image-03.png` | `0:2440` | `363 × 182` | 与 `image-area-mtb-bike-02.png` 同类，保留兼容旧引用 |

Guidance:

- Best choice for product listing pages.
- Compose with editable title, description, price, and CTA.
- Keep card background white and radius 12px.
- For editable product cards, the bike must remain complete. Do not use cover-cropping that cuts wheels, seat, handlebar, basket, or rear rack.

## Best For Bike Cutouts

Use these when a page needs a floating bike image inside a custom-designed composition.

| Asset | Figma Node | Size | Recommended Use |
|---|---:|---:|---|
| `assets/images/real-road-bike-cutout.png` | `0:2398` | `247 × 177` | 真实公路车抠图，适合自定义海报/商品图片区 |
| `assets/images/cutout-bike-display-01.png` | `0:2418` | `277 × 208` | 真实车型展示抠图/展示区，适合重组卡片 |

Guidance:

- Put cutouts on light gray studio backgrounds.
- Add subtle oval wheel shadow if the background does not include one.
- Do not use cutouts alone on plain white without grounding/shadow.

## Best For Small Recommendation Entries

Use these for `口令码`, `Ebike`, `公路车`, `折叠车`, `儿童车`, `骑行服装` entry tiles.

| Asset | Figma Node | Size | Recommended Use |
|---|---:|---:|---|
| `assets/images/figma-bike-variant.png` | `0:1893`/similar | small | 小尺寸车型入口、横滑推荐入口 |
| Generated SVG fallback assets | local | variable | 小入口图不够时补位 |

Guidance:

- Keep small images partially overlapping on the right side of `132 × 60` tiles.
- Do not use full product-card images inside these tiles.

## Generated SVG Fallback Assets

Use these only when a real Figma vehicle asset does not fit the requested category.

| Asset | Use |
|---|---|
| `assets/images/road-bike.svg` | 公路车、竞速车、Madone-like card fallback |
| `assets/images/mountain-bike.svg` | 山地车、越野、户外路线 fallback |
| `assets/images/ebike.svg` | Ebike、电助力、通勤 fallback |
| `assets/images/folding-bike.svg` | 折叠车、城市便携 fallback |
| `assets/images/kids-bike.svg` | 儿童车、亲子出行 fallback |

## Not Recommended As Primary Vehicle Assets

Avoid using these as main vehicle images:

- Route/map thumbnails such as `image 621`.
- Store photos such as `74080... 1` under `门店`.
- Full order/payment page screenshots such as `IMG_6417 1`.
- Tiny icon or 1×1 exports caused by rotated/cropped nodes.
- Shadows alone such as nodes named `投影`.

## Selection Rules

1. For a homepage or campaign page, use `cover-rider-spring-road.png` or `real-home-banner.png`.
2. For fastest high-fidelity product mockups, use complete card assets.
3. For editable product cards, use image-area assets plus editable text/price/button.
4. For custom composition, use cutout assets over a studio background.
5. For category shortcut entries, use small variant images or SVG fallback.
6. Avoid using screenshots of non-product flows as product images.
