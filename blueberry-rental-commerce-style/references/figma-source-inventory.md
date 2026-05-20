# Figma Source Inventory

This file records the two Figma sources behind the Blueberry Skill so future calls can select the right page skeleton and asset source faster.

## Source A: Blueberry Style File

| Field | Value |
|---|---|
| File | `蓝莓风格抓取` |
| File key | `dH2JvWGtFd1PnezyJm6YC5` |
| Main page node | `0:1` |
| Detail/component scan node | `2:3569` |
| Observed node count | about `10,234` frame/group/component nodes |

### Page Families Found

| Family | Representative nodes | Use in Skill |
|---|---|---|
| Home / discovery | `首页`, `顶部banner`, `精选热门`, `更多好车`, `底部` | Homepage and discovery screens |
| Rental list | `租车`, `更多好车`, `标题筛选`, `大分类Tap` | Rental vehicle list pages |
| Used bike list | `二手车` | Used-bike marketplace list |
| Curated goods list | `甄选好物`, `甄选好物-双列` | Goods/accessory mall list; single-column and two-column variants |
| Product rail card | `选车`, `车1`, `Frame 1912055180`, `文案`, `价格`, `More` | Horizontal vehicle recommendation rail |
| Vehicle detail | `车辆详情`, `商品图`, `价格条`, `选车卡`, `更多参数`, `商家1`, `nav` | Store reservation / inspection detail page |
| Tabs and filters | `Tabs 选项卡-应用`, `筛选菜单`, `筛选标签`, `类型`, `租赁价`, `排序` | Category and list filters |
| Bottom navigation | `底部`, `Functional category`, `Home Indicator`, `底部导航小横条` | Persistent navigation and bottom bars |
| Order and pickup states | `待取车`, order cards, payment/deposit annotations | Post-order and fulfillment pages |
| Rider information | `添加骑行人信息`, `身份证`, `Radio icon`, `standard input` | Rider forms and rider selection sheets |
| Dialogs and feedback | `弹窗`, `Toast`, `Picker 选择器` | Confirmation, picker, and feedback states |

### Important Page Skeletons

#### Home / Discovery

Use:

1. Status bar.
2. Large image banner, about `390 × 458`.
3. Primary tabs over/near banner.
4. Horizontal quick entries.
5. Product rail or product cards.
6. Bottom navigation.

#### Vehicle List / Curated Goods

Use:

1. Status bar.
2. Brand/title row.
3. Channel tabs: `租车`, `二手车`, `自研产品`, `甄选好物`, `友商合作`.
4. Filter chips: `类型`, `租赁价`, `排序`.
5. Optional category shortcut pills.
6. Section header and product list.
7. Fixed bottom nav.

There are two known list variants:

- Single-column large card feed for high-value rental items and vehicles.
- Two-column card grid for goods/accessories where density matters.

#### Product Rail Card

Use for homepage or recommendation rails:

- Card about `329 × 446`.
- Image area about `329 × 278`.
- Copy block at about `y=301`.
- Price/footer at about `y=385`.
- CTA pill `选TA`.

#### Vehicle Detail

Use:

1. Product image area.
2. Dedicated rental price strip.
3. Product title.
4. Selection card.
5. Parameter card.
6. Store card.
7. Product intro.
8. Bottom CTA.

Do not merge this with the list page or homepage hero.

#### Order / Rider / Payment

Use quiet operational pages:

- 390px canvas.
- Standard title/status bar.
- White rows/cards.
- Fixed bottom CTA.
- Rider rows around `358 × 66`.
- Bottom sheet / picker for selections.

## Source B: SKU Asset File

| Field | Value |
|---|---|
| File | `sku 色值` |
| File key | `0LqKNUZkd4ZOb1J8HlD9gI` |
| Page node | `0:1` |
| Observed asset-like frames | about `632` frames at `328 × 190` or `800 × 800` |

### Observed Asset Categories

| Category | Approx count | Examples |
|---|---:|---|
| 公路 / 平把 | `93` | `Allez`, `Tarmac`, `Domane`, `Sirrus`, `竹子平把公路` |
| 电助力 / 蓝莓自研 | `88` | `蓝莓 Aurora`, `蓝莓 JOY`, `EBI AGILE`, `宇宙 E-Bike Nomad` |
| 折叠车 / 小布 | `69` | `G Line`, `P Line`, `C Line`, `小布装车箱` |
| 儿童车 | `21` | `Precaliber`, `Riprock`, `Jett` |
| Cargo / 生活车 | `11` | `CarGO Bike`, `Car go 生活自行车` |
| 配件 / 服务商品 | `3+` | `头盔租赁`, `相机`, `定金` |
| Other / uncategorized | many | Color-only or template nodes requiring manual review |

### Asset Size Rules

- `328 × 190` frames are best for card image areas, list cards, and direct Figma-style product assets.
- `800 × 800` frames are best for high-resolution detail hero extraction, future clean cutouts, and premium cards.
- `80 × 80` / `82 × 82` nodes are color thumbnails or small SKU chips.

### Asset Selection Priority

1. Use already cleaned local `assets/images/sku-clean/` assets for detail hero and custom layout.
2. Use local `assets/images/composite/` assets for product-card image regions.
3. If a needed model/color is missing locally, export the corresponding Figma node from `sku 色值`, clean it, and add it to `sku-clean/`.
4. Use original Figma `328 × 190` frames only when reproducing a card image block exactly.
5. Use SVG placeholders only if no matching real SKU asset exists.

### High-Value Export Backlog

Prioritize these if more real assets are needed:

- 公路车: `Tarmac SL8 Expert 蓝色`, `Tarmac SL8 Comp 黑色`, `Allez Sport 黑色`, `Domane AL2`, `Madone SL5`.
- 折叠车: `C Line`, `P Line`, `G Line` in multiple colors and sizes.
- 电助力: `蓝莓 Aurora`, `蓝莓 JOY`, `EBI AGILE`, `宇宙 E-Bike Nomad`.
- 生活车: `CarGO Bike` variants.
- 配件: `头盔租赁`, `相机`, `小布装车箱`, `定金`.

## Self-Check Result

The current Skill has the correct visual direction, but future generation should rely on both sources:

- Use `蓝莓风格抓取` for page structure, density, modules, and component hierarchy.
- Use `sku 色值` for real vehicle/product visuals and color/model coverage.
- Do not infer page layout from SKU assets.
- Do not infer vehicle/category coverage from the Blueberry style file alone.
