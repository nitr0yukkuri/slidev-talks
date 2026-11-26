# Field Notes — design direction

Slidair-inspired visual treatment, not a port of Slidair. Use local CSS, inline SVG and standard Slidev features. No separate editor, weather system, WebGL or image downloads.

- Cover: midnight ink, a quiet teal edge glow, serif headline.
- Section: muted forest, sparse curves and generous space.
- Content: warm paper and dark ink; artwork is nearly invisible.
- Code: dark surface and a dedicated code area.
- Quote: muted violet, centered typography.
- Closing: subdued amber, a quiet ending.

The graphics are deliberately static so each slide stays consistent between presentation, overview and export. Fonts are system fallbacks with external providers disabled; actual glyph metrics vary by OS. Install a Japanese serif/sans font locally if missing.

Use `layout: atmos-content` (or cover/section/code/quote/closing) with optional `kicker` in the slide frontmatter. Use Markdown, Vue and Slidev click animations as usual. Keep one message per slide; content is not auto-shrunk. Check the exported deck and long Japanese headings on the actual presentation PC.

Reference: https://github.com/nitr0yukkuri/slidair
