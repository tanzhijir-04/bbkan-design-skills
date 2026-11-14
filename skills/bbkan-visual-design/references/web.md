# Web design reference

Use this reference for responsive websites and web interfaces in the BBKan visual style.

## Composition

- Establish a calm paper canvas and a clear reading column. Use a blue title bar, compact metadata, and thin dividers to create editorial structure.
- Use cards and panels to group meaningful content. Give important actions clear labels and enough space; do not turn every item into a bordered box.
- Keep navigation concise. Blue should identify the frame or active section; orange should draw attention to a primary action or a specific annotation.
- Use a consistent spacing rhythm based on multiples of 4 px where practical. Let larger gaps distinguish sections.

## Components and interaction

- Use squared corners or a small radius. Avoid glossy gradients, soft floating shadows, and pill-shaped controls unless the product already depends on them.
- For a tactile button, use a crisp border with a light inset edge on the top/left and a darker edge on the bottom/right. Show a pressed state by shifting the control a small amount or changing the hard shadow; keep focus clearly visible.
- Provide hover, focus-visible, active, disabled, and selected states where relevant. Do not communicate state through color alone.
- Use a readable body size and line height. Reserve monospaced typography for short labels, timestamps, counts, and navigation metadata rather than long prose.
- In dark mode, switch the surface and text tokens together; check muted text, rules, borders, and focus indicators independently.

## Responsive behavior

- Reflow editorial columns into a single readable column at narrow widths. Keep the title, primary action, and content identity visible without horizontal scrolling.
- Let card grids reduce columns naturally. Keep tap targets comfortable and preserve clear separation between adjacent actions.
- Use fluid type only within a deliberate range; long Chinese and Latin text should wrap without clipping or overlap.
- Check the actual design at a desktop width and a narrow mobile width. Verify keyboard focus, contrast, and reduced-motion behavior when motion is present.

## Finish

Use [../assets/bbkan-theme.css](../assets/bbkan-theme.css) for starting tokens and border helpers. Treat the file as optional; map the values into the host project's existing token system when one exists.
