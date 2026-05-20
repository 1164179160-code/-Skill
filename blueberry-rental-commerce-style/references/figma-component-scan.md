# Blueberry Figma Component Scan

Source: `蓝莓风格抓取`

| Field | Value |
|---|---|
| Figma file key | `dH2JvWGtFd1PnezyJm6YC5` |
| Scanned node | `2:3569` |
| Node name | `蓝莓的商品详情页` |
| Scan date | `2026-05-19` |

## Component Inventory

The scanned node contains one production-like vehicle detail page plus surrounding component samples.

| Component group | Figma evidence | Skill usage |
|---|---|---|
| Vehicle detail page | `车辆详情`, `商品图`, `Name`, `Group 44`, `Group 43`, `Group 41`, `nav` | Default detail-page skeleton and quality benchmark |
| Product hero | `商品图` at `342 × 220`, image group, carousel dots | Large transparent bike hero; no text/price overlay |
| Price strip | Dark strip around `y=371`, day/hour rent text | Mandatory detail price row below hero when rental price exists |
| Selection card | `Group 44`, color, handlebar, size, hint tag | Color/variant/size card pattern |
| Parameter card | `Group 43`, two-column spec fields | Equipment/spec inspection module |
| Store card | `商家1`, address, distance, business state | Store availability and pickup/return module |
| Fixed bottom action | `nav`, `预约租赁`, `咨询` | Fixed bottom bar with black primary CTA |
| Tabs and filters | `Tabs 选项卡-应用`, `筛选菜单`, `筛选标签` | Category and mall filter scaffolding |
| Vehicle list / curated goods | Primary channel tabs, filter chips, shortcut category pills, product card feed | `租车` / `甄选好物` / mall browsing list pages |
| Liquid Glass controls | `Liquid Glass - Medium`, brand/price/sort filter pills | Filter pills and bottom nav glass treatment |
| Bottom toolbar/nav | `底部工具栏`, `Functional category`, `底部导航小横条` | Persistent action and nav zones |
| Buttons | `Button`, `按钮区域`, `Basic_ Toolbar` | Primary/secondary CTA specs |
| Dialogs and pickers | `弹窗`, `Picker 选择器`, `item/option` | Order, time, location, confirmation overlays |
| Tags | `标签`, `更高性价比`, `租车越久越划算`, `新手推荐NO.1`, `营业中` | Recommendation/availability/rental-value tags |

## Extracted Layout Rules

- Detail page reference width is `375px`; general generation can still use the Skill's `390px` mobile canvas when matching newer Blueberry marketplace pages.
- Detail hero is a clean product inspection area. The vehicle stays centered, fully visible, and separated from title and price.
- The rental price strip is a horizontal band below the hero, not a floating badge beside the vehicle.
- Detail content uses white rounded cards with `24px` side inset in the `375px` reference and about `327px` card width.
- Selection card uses compact 26px color swatches, 64px option tiles, and small dark-blue helper tags.
- Bottom action bar is fixed and functional, with the primary CTA occupying most of the width.
- Filters use glass-like rounded pills around `80-94px × 32px`, and tabs use a 44px high row.
- Pickers use a `390 × 330` bottom sheet, 58px title row, 200px wheel area, and 72px toolbar.
- The vehicle list page should be treated as its own page template: brand row, channel tabs, filter chips, shortcut category pills, section title, then product cards.

## Skill Implications

- Add this scan as the component-level reference after `blueberry-fidelity.md`.
- Use Figma component names as vocabulary when generating: `车辆详情`, `商品图`, `价格条`, `选车卡`, `更多参数`, `商家卡`, `筛选菜单`, `Picker`.
- For future high-fidelity work, prefer reconstructing these components before creating new decorative modules.
- Vehicle detail pages should follow the scanned structure unless the user explicitly asks for a full marketplace transaction variant.

## Cross-Page Style Calibration

This scan should be interpreted together with the previously captured Blueberry pages and SKU asset rules.

Blueberry's core style is not a poster-first or campaign-first style. It is a light rental-commerce system where product photography creates trust, while transaction modules create hierarchy.

### Strongest Page-Level Rules

- The first screen can show a large product image, but it should remain an inspection area, not an advertising poster.
- The rental price and product title should be separated from the image. Use a price strip or a product information card.
- Important business modules appear in this order on vehicle detail pages:
  1. Product image.
  2. Rental price.
  3. Product title.
  4. Selection and availability.
  5. Store or fulfillment information.
  6. Parameters and product intro.
  7. Fixed bottom CTA.
- Blueberry pages use white cards and soft gray page backgrounds, but the cards are compact and functional.
- Black primary CTA is the conversion anchor. Avoid bright cyan or colorful marketplace CTAs unless explicitly requested.
- Liquid Glass is used for navigation and filter controls, not as a decorative effect everywhere.

### Component Priority

When generating a Blueberry page, rank components by importance:

1. `商品图` and clean vehicle asset.
2. `价格条` or product price information block.
3. `选车卡` with color/size/variant.
4. `商家卡` or fulfillment information.
5. `底部 CTA`.
6. `Tabs/筛选` for list and category flows.
7. `Picker/弹窗` for time, city, store, and confirmation flows.

### Anti-Drift Notes

- Do not make the vehicle tiny in a huge blank area.
- Do not place the vehicle inside a visible white PNG rectangle when a transparent clean asset exists.
- Do not use large marketing headlines on detail/list pages.
- Do not use decorative gradients to replace the scanned dark price strip.
- Do not copy third-party marketplace visual language when only the header structure is requested.

## Current Gaps To Improve Later

- Direct export of the original component screenshots from this node would improve visual QA.
- Component-level HTML templates for `Tabs`, `筛选菜单`, `Picker`, and `弹窗` should be added if these flows are requested often.
- The Skill currently has good SKU assets, but should continue replacing low-resolution or halo-heavy vehicle PNGs when cleaner Figma exports are available.
