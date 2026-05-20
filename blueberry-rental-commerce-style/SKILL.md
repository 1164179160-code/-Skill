---
name: blueberry-rental-commerce-style
description: Generate, critique, or refine Blueberry cycling rental-commerce mobile interfaces and H5 prototypes using Figma-derived page structures, Blueberry visual rules, real vehicle PNG assets, rental-commerce interaction logic, and scenario-specific state handling. Use when creating or improving Blueberry rental mall pages, vehicle/category lists, product cards, vehicle detail pages, Dewu-structure-inspired product headers, reservation/calendar flows, order confirmation, rider information sheets, payment/deposit pages, filter sheets, bottom sheets, PRDs, user journeys, or design reviews that should follow the light premium Blueberry riding style with large real bike imagery, white rounded cards, black capsule CTAs, compact commerce typography, soft gray surfaces, horizontal discovery entries, and Liquid Glass bottom navigation.
---

# Blueberry Rental Commerce Style

Use this skill to produce light, premium cycling rental-commerce interfaces based on the Blueberry riding Figma file and the extracted SKU vehicle asset file. The output should support realistic rental and shopping decisions, not just visual mood: users need to inspect the vehicle, understand price and stock, choose color/size safely, select rental dates in the right step, and complete reservation or purchase actions.

## Fidelity Goal

Outputs should look like they belong in the original Blueberry Figma file, not merely "inspired by" it. When uncertain, prioritize exact Blueberry layout patterns: 390px mobile canvas, large photographic bike/product areas, white rounded product cards, black capsule CTAs, compact commerce typography, horizontal discovery rails, and Liquid Glass bottom navigation.

The goal is high visual fidelity to the production Blueberry design. Do not invent new layout systems when an online/reference pattern exists. Use the reference page skeletons, component ratios, and asset rules as constraints, not loose inspiration.

## Core Workflow

Think like a rental-commerce product designer first, then use the reference files to make the solution consistent and executable. Do not jump directly from the request to visual styling.

1. **Understand the request and scenario.** Read `references/request-analysis.md` for page-generation, redesign, PRD, or review tasks. Infer the page type, user, entry point, primary task, rental/purchase decision, required content, risk of wrong selection, and state coverage. Ask only when a missing answer would materially change page structure.
2. **Frame the page problem.** Decide the first-viewport priority, information hierarchy, primary CTA, secondary actions, and success path. Use `references/page-style-library.md` to select the closest Blueberry page framework.
3. **Choose the output mode.** Default to interactive H5 HTML/CSS/JS when the user asks to generate a page or prototype. Use PRD/user-journey/flow output only when requested. Use Figma-oriented strategy when the user asks for design-file planning or Figma continuation.
4. **Select the page skeleton.** Read `references/blueberry-fidelity.md` and `references/high-fidelity-generation.md`. Use the matching Blueberry skeleton: home/discovery, vehicle list, marketplace detail, reservation detail, order sheet, rider sheet, payment/deposit, or store module.
5. **Select assets by component.** Read `references/sku-vehicle-assets.md` and `references/assets.md` before choosing vehicle images. Use `assets/images/sku-clean/` for large transparent detail heroes, `assets/images/composite/` for product cards and recommendation cards, and Figma-captured PNGs when reproducing an existing block.
6. **Build the interaction model.** Use `references/interaction-states.md` for filtering, selection, reservation, rider info, payment, stock, unavailable, loading, empty, and success states. Detail pages should not duplicate rental-duration cards when the production flow selects dates after tapping the reservation CTA.
7. **Implement or describe the artifact.** Start from a 390px mobile canvas with Blueberry light surfaces, real product imagery, white rounded cards, compact commerce text, black capsule CTAs, and safe-area aware fixed actions. Include lightweight JavaScript for key interactions in H5 prototypes.
8. **Improve visual quality.** Read `references/visual-quality.md` for page-level anchor, image scale, hierarchy, rhythm, and polish. Keep the page Blueberry-specific rather than generic AI mobile UI.
9. **Stress test correctness.** Read `references/design-correctness.md` and verify the scenario, selection logic, inventory/date constraints, and conversion path still work.
10. **Review before delivery.** Use `references/review-checklist.md`, `references/anti-generic-ai.md`, and the high-fidelity checklist in `references/blueberry-fidelity.md` before finalizing.

## Output Modes

Default to an interactive H5 prototype when the user asks to generate a page, draw a prototype, open a preview, or make a visual page.

- **Interactive H5 prototype**: Generate standalone HTML/CSS/JS with Blueberry page structure, local assets, selected/disabled/loading states, clickable tabs, color/size selection, filter sheets, date/calendar sheets, and bottom CTA interactions. Use this for fast browser preview.
- **PRD or user journey**: Structure scenarios by user type, rental stage, trigger, goal, decision, module priority, state, and metric. Use this when the user asks for PRD, journey, flow, or strategy.
- **Design review or redesign advice**: Compare the current page against Blueberry structure, vehicle imagery quality, selection safety, price/stock clarity, and conversion path. Lead with concrete issues and revised hierarchy.
- **Figma strategy**: Describe how to map the page back into Figma components and assets when the user asks for Figma planning or wants to continue in an existing design file.

## Interactive H5 Requirements

When generating H5, include lightweight JavaScript for key interactions instead of drawing only static states.

- Color or vehicle thumbnail selection updates hero image, selected color name, stock copy, and size/store availability.
- Size selection updates selected state and shows guidance such as recommended height range.
- `预约` or `立即预约` opens a calendar/date bottom sheet if the flow requires selecting rental time after CTA.
- Filter chips open sheets or dropdowns; selected filters update visible labels.
- Tabs and segmented controls change active state and visible content.
- Disabled or out-of-stock variants are visibly disabled and cannot be selected without feedback.
- Toast, dialog, or inline notice appears for unavailable date, no stock, validation error, or reservation success.
- Sticky bottom CTA respects safe area and remains visually separate from content.

## Proposal Output Format

For design proposals, include the interface or prototype plus a concise rationale:

- User and scenario.
- User goal and product goal.
- Design strategy.
- Information hierarchy.
- Interaction and state logic.
- Visual rationale.
- Prototype or local file path when generated.

Keep rationale concrete. Name the rental or shopping decision being supported. Avoid generic claims such as "improves experience" unless the explanation says how.

## Priority Order

When references conflict, resolve decisions in this order:

1. Current user request.
2. Blueberry rental-commerce scenario, user goal, and conversion path.
3. `references/page-style-library.md` page framework.
4. `references/blueberry-fidelity.md` production skeleton and measurements.
5. `references/components.md` component rules.
6. `references/sku-vehicle-assets.md` and local asset availability.
7. `references/style-rules.md` visual tokens and typography.
8. `references/interaction-states.md` state and behavior rules.
9. General mobile UX best practices.

Use `references/anti-generic-ai.md` as a final guardrail, not as a source for page structure.

## Reference Files

Read only what is needed:

- `references/style-rules.md`: visual style, color, typography, spacing, imagery.
- `references/request-analysis.md`: scenario analysis before page generation, redesign, PRD, or review.
- `references/page-style-library.md`: page-level frameworks for home, list, detail, reservation, order, payment, and store modules.
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
- `references/visual-quality.md`: page-level visual anchor, hierarchy, rhythm, polish, and Blueberry-specific product expression.
- `references/design-correctness.md`: rental-commerce correctness checks for user goal, product goal, selection, stock, reservation, and conversion.
- `references/anti-generic-ai.md`: final guardrail against generic AI mobile UI.
- `references/review-checklist.md`: final self-review checklist before delivery.

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
