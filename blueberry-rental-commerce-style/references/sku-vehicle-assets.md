# SKU Vehicle Assets

These assets were extracted from the Figma file `sku 色值`.

Use this file before selecting any generated SVG fallback. These images are real SKU/product exports and should be the default source for realistic Blueberry vehicle pages.

## Source

| Field | Value |
|---|---|
| Figma file | `sku 色值` |
| File key | `0LqKNUZkd4ZOb1J8HlD9gI` |
| Full page node | `0:1` |
| Observed asset-like frames | about `632` |
| Preferred clean export folder | `assets/images/sku-clean/` |
| Transparent export folder | `assets/images/sku-transparent/` |
| Preferred composed folder | `assets/images/composite/` |
| Original export folder | `assets/images/sku/` |
| Export size | about `328 × 190` PNG |

## Full Source Coverage

The Figma source contains far more assets than the local cleaned set. Treat the local files as the currently installed subset, not the complete source.

Observed source categories:

| Category | Approx count | Typical model names |
|---|---:|---|
| 公路 / 平把 | `93` | `Allez`, `Tarmac`, `Domane`, `Madone`, `Sirrus`, `竹子平把公路` |
| 电助力 / 蓝莓自研 | `88` | `蓝莓 Aurora`, `蓝莓 JOY`, `EBI AGILE`, `宇宙 E-Bike Nomad` |
| 折叠车 / 小布 | `69` | `G Line`, `P Line`, `C Line`, `T Line`, `小布装车箱` |
| 儿童车 | `21` | `Precaliber`, `Riprock`, `Jett` |
| Cargo / 生活车 | `11` | `CarGO Bike`, `Car go 生活自行车` |
| 配件 / 服务商品 | `3+` | `头盔租赁`, `相机`, `定金` |

Use `references/figma-source-inventory.md` for the broader source map before deciding that an asset is unavailable.

## Asset Table

| Category | Asset | Figma Node | Best Use | Avoid |
|---|---|---:|---|---|
| 公路车 | `assets/images/sku-clean/road-allez-sport-gray.png` | `1:92` | 标准商品卡、车型列表、入门公路车推荐 | 不要放大到全屏首屏海报 |
| 公路车 | `assets/images/sku-clean/road-tarmac-sl8-black.png` | `45:13` | 高端车型卡、进阶推荐、竞速专题 | 不要用于儿童/通勤类目 |
| 折叠车 | `assets/images/sku-clean/folding-g-line-white.png` | `1:3` | 折叠车频道、小布通勤卡、便携场景 | 不要作为公路车推荐 |
| 儿童车 | `assets/images/sku-clean/kids-precaliber-purple.png` | `1:18` | 儿童车、亲子骑行、家庭出行 | 不要和成人公路车价格体系混用 |
| 电助力 | `assets/images/sku-clean/ebike-turbo-vado-sl.png` | `53:171` | 电助力、长距离通勤、高续航推荐 | 不要用于轻量竞速公路车 |
| 电助力 | `assets/images/sku-clean/ebike-cosmos.png` | `59:10` | 生活方式 Ebike、舒适骑行、城市短途 | 不要用于高端竞速卖点 |
| 平把公路车 | `assets/images/sku-clean/flatbar-fx2-red.png` | `1:140` | 平把公路车、城市健身、日常通勤 | 不要归入山地车 |
| 特色车 | `assets/images/sku-clean/special-bamboo-lady.png` | `16:13` | 主题活动、特色车型、海报局部视觉 | 不要作为标准车型列表默认图 |
| 特色车 | `assets/images/sku-clean/special-cargo-life.png` | `281:13` | 家庭载物、生活车、Cargo 场景 | 不要用于竞速/轻量类目 |
| 配件 | `assets/images/sku-clean/accessory-brompton-box-gray.png` | `287:4` | 加购推荐、装车箱、配件横滑卡 | 不要作为车辆主体图 |

## Category Guidance

### 公路车

Use `road-allez-sport-gray.png` for normal product listings and `road-tarmac-sl8-black.png` for premium or advanced cards. Keep the image centered inside a pale gray or white studio area.

### 折叠车

Use `folding-g-line-white.png` for city commuting, subway transfer, compact storage, and Brompton-like page sections. Pair with compact copy and a high convenience value proposition.

### 儿童车

Use `kids-precaliber-purple.png` for family, parent-child, beginner, and safety-oriented sections. Do not mix with aggressive sport copy.

### 电助力

Use `ebike-turbo-vado-sl.png` for premium Ebike cards and `ebike-cosmos.png` for lifestyle or accessible Ebike entries. Pair with range, battery, commute, and easy-riding labels.

### 平把公路车

Use `flatbar-fx2-red.png` for fitness commute and urban riding. It should sit between road-bike and city-bike sections.

### 特色车 / Cargo

Use `special-bamboo-lady.png` and `special-cargo-life.png` as visual variety in special modules, campaign blocks, and story cards. These are good for breaking up repetitive road-bike lists.

### 配件

Use `accessory-brompton-box-gray.png` only in add-on purchase or rental accessory modules.

## Composition Rules

- Product cards: place SKU image in the top 52%-60% of the card, with editable title, metadata, price, and CTA below.
- White display scene: use the PNG as-is on `#F6F7F8` or `#FFFFFF`; keep at least 18px side padding.
- Always show the complete vehicle body. Use `object-fit: contain`, keep both wheels visible, and never crop the front wheel, rear wheel, saddle, handlebar, or cargo basket to fill the card.
- Use `sku-clean` assets for UI composition. They are based on `sku-transparent` but have cleaner edges and less white/gray halo.
- Original `sku` files include white backgrounds and should not be placed on gray studio surfaces unless the whole image area is intentionally white.
- For large vehicle detail hero areas, use `sku-clean` directly so the bike can be large and has no visible image block. For cards and rails, use pre-composited PNGs from `assets/images/composite/` whenever available.
- Cover poster: SKU PNGs are not full campaign photos. Use them with a large white/light-gray studio surface, oversized typography, and product swatches, not as full-bleed lifestyle photography.
- Recommendation rail: crop gently, keep the whole vehicle readable, and avoid cutting wheels.
- If using multiple SKU assets on one page, do not repeat the same category more than twice before mixing in another category.

## Known Additional Candidates In The Same Figma File

The source file also contains more vehicle SKUs that can be exported later if needed:

| Category | Node / Name |
|---|---|
| 公路车 | `1:71` Allez 褐红色, `59:50` Allez Sport 黑色, `1:96` Madone SL 5 Gen 8 亮白色, `1:87` Madone SL 5 Gen 8 白色, `45:23` Tarmac SL8 Expert 蓝色, `1:158` Tarmac SL7 Sport 白粉色, `45:66` Domane AL 2 红色 |
| 折叠车 | `1:55` G line 森林绿, `1:60` G line 探险橙, `1:8` P line 冲刺绿, `1:45` P line 电光蓝, `1:50` P line 霓虹海洋色 |
| 儿童车 | `1:23` Precaliber 24 海军蓝, `1:40` Precaliber 24 夏威夷绿, `1:28` Riprock Coaster 16 红色, `1:34` Riprock Coaster 16 蓝色 |
| 电助力 | `329:138` EBI AGILE LowFrame 白, `329:152` EBI AGILE 红, `329:161` EBI AGILE 黄 |
| 平把公路车 | `44:3` Sirrus X 2.0 紫色, `1:146` Sirrus X 2.0 柠檬黄, `1:152` Sirrus X 5.0 黑色, `48:150` Sirrus X 2.0 白色 |
