**CREATE DESIGN SYSTEM JSON**

UI TO ANALYZE: $ARGUMENTS

**GOAL**
Your goal is to extarct a generalized and reusable design system from the screenshot provided in `$ARGUMENTS`, **without including specifc image content**, so that frontend develoeprs or AI agents can reference the JSON as a style foundation for building consistent UIs.

**Task**

1. Analyze the screenshots provided in to infer:

- Color palette
- Typography rules
- Spacing guidelines
- Layout structure (grids, cards, containers, etc.)
- UI Components (buttons, inputs, tables, etc.)
- Border radius, shadows, and other visual styling patterns

2. Create a `design-system.json` file that clearly defines these rules and can be used to replicate the visual language in a consistent way.

3. Output the JSON to the root of the project with the name: `design-system.json`

**CONSTRAINTS**

- DO **NOT** extract specific content from the screenshots (no text, logos, icons)
- Focus purely on _design principles_, _structrue_, and _styles_.
