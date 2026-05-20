# Blueberry Local Assets

Use these bundled assets when generating Blueberry-style pages, especially when product photos are unavailable or Figma image URLs are not accessible.

For usage classification, read `references/sku-vehicle-assets.md` and `references/vehicle-assets-classification.md`.

## Bike Images

Assets are under `assets/images/`.

### Figma-captured Assets

These are captured from the Blueberry Figma file and should be preferred for highest fidelity.

### SKU Vehicle Assets

These are real product exports from the Figma file `sku 色值`. Use the cleaned transparent-background versions before generated SVGs whenever a page needs realistic bike imagery.

### Composited Product Scene PNGs

These are pre-composited PNG scenes built from transparent SKU images plus studio background and tire shadow. Prefer them for product cards, recommendation cards, and marketplace image areas where the image region should be stable and polished. Do not use them for large detail hero areas that require a transparent vehicle without a visible image block.

| Asset | Use |
|---|---|
| `assets/images/sku-clean/*.png` | 去白底和边缘白边后的干净车型图。详情页大图优先使用。 |
| `assets/images/composite/detail-hero-tarmac-sl8.png` | 车辆详情页顶部大图 |
| `assets/images/composite/detail-rec-allez-sport.png` | 详情页同类推荐卡、辅助入口 |
| `assets/images/composite/detail-rec-fx2-red.png` | 详情页同类推荐卡 |
| `assets/images/composite/detail-rec-turbo-vado.png` | 详情页同类推荐卡 |
| `assets/images/composite/mall-hero-tarmac-sl8.png` | 商城车型页精选推荐区 |
| `assets/images/composite/mall-card-allez-sport.png` | 商城商品列表图 |
| `assets/images/composite/mall-card-turbo-vado.png` | 商城商品列表图 |
| `assets/images/composite/mall-card-folding-gline.png` | 商城商品列表图 |
| `assets/images/composite/mall-card-cargo-life.png` | 商城商品列表图 |

| Asset | Use |
|---|---|
| `assets/images/sku-clean/road-allez-sport-gray.png` | 公路车标准商品图、白底车型卡、入门公路车推荐 |
| `assets/images/sku-clean/road-tarmac-sl8-black.png` | 高端公路车、竞速车型、会员/进阶推荐卡 |
| `assets/images/sku-clean/folding-g-line-white.png` | 折叠车、城市通勤、小布/Brompton 类目 |
| `assets/images/sku-clean/kids-precaliber-purple.png` | 儿童车、亲子骑行、低龄车型卡 |
| `assets/images/sku-clean/ebike-turbo-vado-sl.png` | 电助力、长距离通勤、高续航推荐 |
| `assets/images/sku-clean/ebike-cosmos.png` | 电助力/生活方式车型、轻松骑行推荐 |
| `assets/images/sku-clean/flatbar-fx2-red.png` | 平把公路车、城市健身、轻运动通勤 |
| `assets/images/sku-clean/special-bamboo-lady.png` | 特色车、活动海报、主题内容入口 |
| `assets/images/sku-clean/special-cargo-life.png` | Cargo/生活车、家庭出行、载物场景 |
| `assets/images/sku-clean/accessory-brompton-box-gray.png` | 骑行配件、小布装车箱、加购推荐 |

| Asset | Use |
|---|---|
| `assets/images/real-home-banner.png` | Real homepage poster/banner from Figma. Use for Blueberry home or category hero. |
| `assets/images/real-road-bike-cutout.png` | Real road-bike transparent/cutout export from the Figma product card. Prefer this for product cards. |
| `assets/images/real-road-bike-image-area.png` | Real Figma card image area background export. |
| `assets/images/real-road-bike-card.png` | Complete Figma product card export for reference or exact mockups. |
| `assets/images/real-product-card-02.png` | Complete second Figma product card export. |
| `assets/images/real-product-image-03.png` | Real product image area export for another card. |
| `assets/images/figma-card-bg.png` | Product card studio background from Figma |
| `assets/images/figma-road-bike.png` | Real Figma bike/product cutout |
| `assets/images/figma-bike-variant.png` | Small bike/variant asset captured from Figma |
| `assets/images/figma-color-swatches.png` | Figma color swatch strip asset |

### Generated SVG Backup

| Asset | Use |
|---|---|
| `assets/images/road-bike.svg` | 公路车、竞速车、精选车型、Madone-like product cards |
| `assets/images/mountain-bike.svg` | 山地车、越野、户外骑行、进阶路线 |
| `assets/images/ebike.svg` | Ebike、电助力、通勤短租、轻松骑行 |
| `assets/images/folding-bike.svg` | 折叠车、城市通勤、便携车 |
| `assets/images/kids-bike.svg` | 儿童车、亲子出行、安全骑行 |

## Usage Rules

- Prefer cleaned transparent SKU PNG assets from `assets/images/sku-clean/` for detail heroes and custom composition.
- Prefer `assets/images/composite/` when building polished product cards and recommendation image areas; avoid rebuilding shadows and studio backgrounds with ad hoc CSS. Do not use composite PNGs for large detail heroes that need no background block.
- Do not place original white-background SKU PNGs directly on gray studio surfaces; they create visible white blocks.
- Prefer `real-home-banner.png`, `real-road-bike-card.png`, and `real-product-card-02.png` for full Blueberry homepage/card fidelity.
- Use generated SVG assets only when no SKU or Figma-captured product image fits the category.
- Place them inside pale gray/white studio product image areas.
- Keep them large and centered in product cards.
- Show the complete bike in product cards; use contain-fit image placement with padding instead of cover-fit cropping.
- Add subtle oval shadows under wheels if the target canvas does not already include shadows.
- Do not recolor them into ZD10 dark/red hardware style.
- If a page contains multiple products, vary bike assets by category instead of repeating one image.
