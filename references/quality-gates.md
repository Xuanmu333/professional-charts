# Quality gates

Apply every relevant gate before delivering a chart. Passing a file-format check is not enough; inspect the rendered artifact.

## Data correctness

- Recalculate displayed totals, subtotals, shares, differences, and CAGR from the source values.
- Verify units, currencies, time intervals, category order, signs, and denominators.
- Confirm that every displayed metric name, acronym expansion, segment definition, and threshold is supplied or explicitly confirmed rather than inferred.
- Confirm that each change annotation uses the endpoints and interval named by its wording. A full-series change must not be described as a post-event change.
- Recalculate any acceleration, slowdown, or slope-change claim over comparable intervals. Confirm that a one-period event jump has not been mislabeled as a sustained rate change.
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
- Event separators align to the stated date or period, and any shaded observation region spans the intended interval without implying unsupported causality.
- Color meaning remains consistent, and the emphasized mark is the one that supports the title.

## Readability

- No label, title, source, arrow, marker, or legend overlaps another object.
- No text is clipped, wrapped awkwardly, or pushed outside the slide or canvas.
- When a subtitle exists, the title and subtitle remain visually separate, with a gap of at least half the subtitle line height; the subtitle also retains at least one line height of whitespace before the chart or legend.
- Multi-line titles and subtitles use readable line height rather than compressed leading, and the plot area has been moved or reduced instead of squeezing the title block.
- Across all chart types, no endpoint guide, comparison bracket, connector, arrow, or leader touches or crosses a value label. Verify visible clearance at bar and column ends, line and area endpoints, labeled scatter or bubble points, combination-chart marks, Gantt annotations, and waterfall totals.
- Direct labels clearly map to their marks; leader lines do not cross unnecessarily.
- Direct series labels retain material qualifiers such as units, thresholds, scenarios, or segment definitions needed to interpret the chart.
- The same endpoint or event value is not printed twice beside one mark, and the same event name is not redundantly repeated on the axis and in a nearby callout.
- When series would be ambiguous without color, restrained marker shapes, line styles, or another redundant cue keep them distinguishable.
- No leader arrow points to a single bar that is already identified by accent color and a direct label unless the arrow encodes an additional, nonredundant relationship.
- Numbers use consistent precision and abbreviations.
- Essential text and graphical marks meet the contrast thresholds in the visual grammar; source notes and caveats remain readable after export and downscaling.
- The chart remains legible in a full-slide render, not only when zoomed in.
- Decorative effects do not compete with the data.

## Message fidelity

- The title matches what the data actually supports.
- Causal verbs are used only when causality is supported or explicitly supplied; otherwise the title and annotations describe timing, association, or the observed pattern.
- A metric movement is not relabeled as a specific mechanism such as churn, adoption, or price unless the available measure supports that interpretation.
- “Statistically significant” appears only with a stated supporting test; an untested visual difference or business-threshold comparison is not described as statistically significant.
- The main comparison can be identified without reading a long paragraph.
- Repeated appearances across the title, subtitle, axis, event marker, annotation, or footnote each add distinct information such as timing, value, relationship, or qualification; otherwise remove the duplicate.
- Caveats that could change the conclusion remain visible.
- Sources and the scope of the data are present when known, and no source or provenance is invented.

## Output and delivery

- The delivered file opens successfully in its target application and contains the expected chart content.
- The output matches the requested format and does not silently create a PowerPoint or presentation artifact.
- The final chart has been rendered or exported and visually inspected at full size.
- A standalone raster with no requested dimensions is at least 1600 px wide or exported at 2× its logical layout size. Also inspect it at the intended display width, or at 1280 px width when the destination is unknown, so essential text remains readable after downscaling.
- Any delivered preview matches the source chart with no missing fonts, shifted objects, or changed values.
- Describe the result by its chart type, analytical purpose, and material output limitation without attributing it to a specific charting tool.

If a gate fails, fix the artifact and render it again. If the available data or output format makes a required gate impossible, disclose that limitation instead of hiding it.
