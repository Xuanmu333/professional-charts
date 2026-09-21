# Quality gates

Apply every relevant gate before delivering a chart. Passing a file-format check is not enough; inspect the rendered artifact.

## Data correctness

- Recalculate displayed totals, subtotals, shares, differences, and CAGR from the source values.
- Verify units, currencies, time intervals, category order, signs, and denominators.
- Confirm that a waterfall reconciles its start, drivers, subtotals, and final total.
- Confirm that percentage stacks total approximately 100% and explain any material exception.
- Confirm that Mekko column widths sum to the plot width and segment heights fill each category as intended.
- Confirm that Gantt bars and milestones align with the stated dates.
- Do not show a percentage change from a zero denominator or a conventional CAGR across zero or negative endpoints.

## Visual integrity

- Bar and column lengths use a zero baseline unless a visible, justified axis break is present.
- Related charts that invite comparison use the same scale.
- A waterfall net-change annotation uses two horizontal dashed endpoint guides and a vertical double-ended difference arrow outside the bridge; it does not arc across the driver bars.
- Bubble magnitude is encoded by area.
- Dual axes are clearly labeled and cannot be mistaken for a common scale.
- Actual and forecast periods are distinguishable without relying on color alone.
- Color meaning remains consistent, and the emphasized mark is the one that supports the title.

## Readability

- No label, title, source, arrow, marker, or legend overlaps another object.
- No text is clipped, wrapped awkwardly, or pushed outside the slide or canvas.
- No comparison line, connector, or arrow touches or crosses a value label. Waterfall start and end totals retain a visible gap between their labels and all endpoint guides.
- Direct labels clearly map to their marks; leader lines do not cross unnecessarily.
- No leader arrow points to a single bar that is already identified by accent color and a direct label unless the arrow encodes an additional, nonredundant relationship.
- Numbers use consistent precision and abbreviations.
- The chart remains legible in a full-slide render, not only when zoomed in.
- Decorative effects do not compete with the data.

## Message fidelity

- The title matches what the data actually supports.
- The main comparison can be identified without reading a long paragraph.
- Every analytical annotation adds information rather than repeating the title.
- Caveats that could change the conclusion remain visible.
- Sources and the scope of the data are present when known.

## Editability and delivery

- Required chart marks, labels, and annotations remain editable in the requested source format.
- The artifact contains no rasterized substitute for an editable chart unless the user explicitly requested a flat image.
- The artifact opens successfully in its target application and contains the expected chart content.
- Bars, labels, lines, arrows, and annotations remain separate editable objects supported by the destination rather than a flattened chart image.
- Any delivered preview matches the editable source with no missing fonts, shifted objects, or changed values.
- Describe the result by its chart type, analytical purpose, and editability without attributing it to a specific charting tool.

If a gate fails, fix the artifact and render it again. If the available data or output format makes a required gate impossible, disclose that limitation instead of hiding it.
