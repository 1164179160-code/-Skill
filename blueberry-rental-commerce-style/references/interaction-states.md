# Blueberry Rental Commerce Interaction States

## Browsing

| State | UI Behavior |
|---|---|
| Landing / home | Large banner first, category tabs, recommendation entry rail, product sections |
| Category selected | Active tab becomes bold/dark; product list changes below |
| Brand selected | Brand/filter item receives active pill/background |
| Product rail scroll | Keep product cards partially visible to indicate horizontal movement |

## Product Selection

| State | UI Behavior |
|---|---|
| Product available | Show product photo, title, rental price, CTA `选TA` |
| Multiple colors | Show color swatches; selected swatch may be slightly larger or outlined |
| CTA tapped | Navigate to detail/order confirmation or update selected product state |
| Loading | Use skeleton or light placeholder; avoid heavy spinners over product images |
| Load failed | Toast with concise error; keep prior content if possible |

## Order And Rider Info

| State | UI Behavior |
|---|---|
| No rider selected | Prompt user before payment; toast or sheet prompt |
| Add rider | Open bottom sheet/form with fixed bottom CTA |
| Multiple riders | List rows with radio selection and edit icon |
| Same rider added | Toast error |
| Network failure | Toast error; do not clear user input |
| Delete rider | Single-row left swipe reveals delete action |

## Payment / Deposit

- Keep payment confirmation clean and white.
- If deposit or insurance confirmation is required, use a focused confirmation sheet.
- Avoid sending C-end users out to third-party pages when the product requirement says backend/manual confirmation handles it.

## Priority Rules

1. Product photo and price must stay visible before secondary copy.
2. Category/filter controls should not displace product cards for too long.
3. Bottom CTA should be fixed in sheets/order confirmation.
4. Toasts are short and functional.

