# Field Notes — design direction

Use the warm paper content slide as the default visual language across the deck. Keep the original content slide's palette, spacing, typography and understated footer. Cover, section, quote and closing still differ in typography and placement, not in the default palette. The background is deliberately quiet: a low-opacity edge glow and subtle SVG curves.

Use `layout: atmos-content` (or cover/section/code/quote/closing) with optional `kicker`. To use the previous dark palette, add `tone: dark` to that slide's frontmatter. The sample deck defaults to light. Code colors follow Slidev's syntax highlighting theme.

No new external fonts, imagery, WebGL or animation dependencies. Fonts are local fallbacks and glyph metrics vary by OS. Content is not auto-shrunk; check long headings, code and the exported deck before presenting.

Reference: https://github.com/nitr0yukkuri/slidair
