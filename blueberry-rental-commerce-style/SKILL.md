---
name: blueberry-rental-commerce-style
description: Generate or extend Blueberry cycling rental-commerce mobile interfaces. Use when creating pages, prototypes, product cards, rental bike marketplaces, cycling category feeds, order flows, rider information sheets, product detail/rental selection pages, or visual designs that should follow the light premium Blueberry riding style with large photographic bike banners, white product cards, black capsule CTAs, soft gray backgrounds, horizontal recommendation entries, and Liquid Glass bottom navigation.
---

# Blueberry Rental Commerce Style

Use this skill to produce light, premium cycling rental-commerce interfaces inspired by the Blueberry riding Figma file.

## Fidelity Goal

Outputs should look like they belong in the original Blueberry Figma file, not merely "inspired by" it. When uncertain, prioritize exact Blueberry layout patterns: 390px mobile canvas, large photographic bike/product areas, white rounded product cards, black capsule CTAs, compact commerce typography, horizontal discovery rails, and Liquid Glass bottom navigation.

The goal is high visual fidelity to the production Blueberry design. Do not invent new layout systems when an online/reference pattern exists. Use the reference page skeletons, component ratios, and asset rules as constraints, not loose inspiration.

## Core Workflow

1. Read `references/blueberry-fidelity.md` and `references/high-fidelity-generation.md` first for any page-generation task.
2. Identify the page type before drawing: marketplace home, category/list, vehicle detail, order sheet, rider sheet, payment/deposit, or store module.
3. Use the matching skeleton in `references/blueberry-fidelity.md`; do not mix unrelated page structures.
4. Read `references/sku-vehicle-assets.md` and `references/assets.md` before choosing vehicle images.
5. Choose image assets by component: use cleaned transparent SKU PNGs from `assets/images/sku-clean/` for large detail heroes that need no image background; use composited PNGs for product cards and recommendation cards that need a stable image area; use Figma-captured PNGs when reproducing an existing visual block.
6. Start from a mobile 390px canvas with a light gray/white commercial surface and exact content insets.
7. Use large real product photography or product-like imagery as the primary visual, especially bikes, cycling gear, or outdoor riding scenes.
8. Keep typography compact and commerce-oriented: strong product name, light metadata, clear price hierarchy.
9. Keep UI clean and bright. Avoid dark immersive device-control styling from ZD10.
10. Before finalizing, run the high-fidelity checklist in `references/blueberry-fidelity.md`.

## Reference Files

Read only what is needed:

- `references/style-rules.md`: visual style, color, typography, spacing, imagery.
- `references/blueberry-fidelity.md`: strict page skeletons, measurements, and anti-drift rules.
- `references/figma-source-inventory.md`: complete source inventory for both Figma files: Blueberry page/component families and SKU asset families.
- `references/figma-component-scan.md`: component inventory and extracted layout rules from the scanned Blueberry Figma node.
- `references/high-fidelity-generation.md`: page-type workflow, asset priority, anti-patterns, and final self-check.
- `references/assets.md`: local SVG bike assets that can be embedded in generated pages.
- `references/sku-vehicle-assets.md`: real SKU vehicle exports from the `sku 色值` Figma file, classified by category and composition use.
- `references/vehicle-assets-classification.md`: classified vehicle image assets from Figma by usage scenario.
- `references/components.md`: banner, recommendation chips, product cards, tabs, bottom nav, sheets.
- `references/interaction-states.md`: browsing, selecting, filtering, rider info, payment/order states.
- `references/copywriting.md`: commerce/rental copy patterns and labels.

## Non-Negotiable Rules

- Use a light theme: white cards, soft gray backgrounds, black primary CTAs.
- Product imagery must dominate product cards; do not replace product photos with abstract decoration.
- Product cards need name, short descriptor, rental price, optional hourly price, and CTA.
- Vehicle detail pages must follow the online-style detail hierarchy: clean white vehicle image area, dark horizontal price strip below the image, product title, selection card, parameter card, store card, and fixed bottom CTA. Do not overlay title or price on the vehicle image.
- If the user references a marketplace app such as Dewu only for the top product area, borrow only the top structure: large product image, thumbnail row, and color/variant entry. Keep the rest of the page in Blueberry's rental-commerce detail structure.
- When borrowing any marketplace structure, keep Blueberry's own visual language: black primary CTA, light gray page, white rounded cards, compact typography, and subdued shadows. Borrow structure, not third-party colors, modules, or brand tone unless explicitly requested.
- When no new real product image is provided, choose by use case: detail hero uses cleaned transparent assets from `assets/images/sku-clean/*.png` enlarged on the page surface with no image block; product cards/recommendation cards use `assets/images/composite/*.png`; captured Figma blocks are used when matching an existing block; generated SVG bike assets are last resort only.
- Do not use generated outline bikes for primary product cards when a matching SKU PNG exists.
- Use rounded 12px cards and black capsule buttons.
- Use horizontal scroll for recommendation entries and product card rails when space is constrained.
- Bottom navigation should feel like translucent Liquid Glass, not a flat dark nav.
- Do not over-design with decorative gradients, oversized type, floating badges, or custom hero layouts if the production pattern is simpler.
- Do not place price/title text on top of vehicle imagery unless the reference page does so.
- Do not use the ZD10 red pixel/hardware-control visual language for this style.
- Do not create dark full-screen hardware controller pages under this skill.
- Do not use red pixel lights, Bluetooth pills, lock sliders, circular hardware controls, or dark device cards.
- Do not rename this skill or merge it with `zd10-device-design-style`.
