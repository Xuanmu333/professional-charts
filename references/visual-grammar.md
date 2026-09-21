# Visual grammar

Use this reference for every professional business chart. These rules describe what must be visible in the final chart, independent of the tool used to create it.

## 1. Message and reading path

- Make one analytical comparison primary. A slide may contain supporting detail, but it must not compete with the main comparison.
- Use a concise factual title when the chart only establishes context. Use a supported takeaway title when the chart proves a specific finding.
- Arrange the reading path as title, primary chart pattern, key annotation, then source or caveat.
- Keep explanatory prose outside the plot unless it points to a specific data mark.

## 2. Direct labels

- Prefer labels next to the data they describe: values inside or just outside bars, series names near line endpoints, and totals above stacks.
- Use a legend only when direct labels would collide, repeat excessively, or make category comparison harder.
- If a label does not fit inside a mark, move it outside and add a thin leader line. Never shrink labels until they become unreadable.
- Maintain a clear association between label and mark. Avoid labels floating in empty space without an anchor.
- Use one number format for values with the same unit. Remove unnecessary decimals and repeat the unit in the axis title or subtitle rather than on every label.

## 3. Analytical annotations

Annotations must encode a real relationship and use the same coordinate system as the chart.

### Absolute difference

For values `a` and `b`:

`difference = b - a`

Show the sign when direction matters. Label a zero difference as `0`, not `+0`.

### Relative difference

`relative difference = b / a - 1`

Do not calculate or display a relative difference when `a = 0`. Explain that the percentage change is undefined or use the absolute difference instead. Treat sign-changing comparisons with care because the conventional percentage can be misleading.

### CAGR

For a positive start value, positive end value, and `n` elapsed periods:

`CAGR = (end / start)^(1 / n) - 1`

Count elapsed intervals, not the number of plotted points. Five annual observations usually contain four annual intervals. Do not show CAGR when either endpoint is zero or negative unless the user supplies a domain-specific convention.

### Shares

`share = part / total`

Verify that all displayed shares use the intended denominator. If rounding prevents labels from summing to exactly 100%, preserve honest rounding rather than silently adjusting a material category. A minor displayed-rounding adjustment is acceptable only when disclosed or immaterial.

### Annotation hierarchy

- Use a difference arrow for a pairwise change.
- Use a CAGR arrow for an average compounded trend over multiple periods.
- Use a value line for a target, average, threshold, or benchmark.
- Use a forecast separator or background distinction for actual versus forecast periods.
- Use straight, orthogonal geometry for endpoint comparisons. Do not use a curved, arcing, or dotted path across the plot unless the path itself encodes an actual trajectory.
- Across every chart family, treat each visible value-label bounding box as a no-draw zone. Comparison lines, endpoint guides, brackets, connectors, arrows, and leaders must remain outside it with a visible gap of at least half the label height. This applies to bar and column ends, line and area endpoints, scatter and bubble labels, combination charts, Gantt annotations, and waterfall totals; no line may touch, cross, or visually split a number.
- When accent color and a direct value label already identify a focal bar, do not add a leader arrow that merely points to that bar. Put any necessary comparison text in the title, subtitle, or adjacent annotation without a pointer.
- Do not repeat the same message in a title, callout, arrow, and footnote.

## 4. Scale integrity

- Start bar and column charts at zero unless a visible axis break is necessary. Never use a hidden truncated axis.
- When related charts invite comparison, use the same physical scale. The same value must occupy the same visual length.
- Make axis breaks conspicuous with a standard break mark and retain enough context to understand the compression.
- Clearly label both axes in a dual-axis chart. Use direct series labels and visually associate each series with its axis.
- In bubble charts, map the third variable to bubble area, not radius.
- Sort categories when ranking is the message. Preserve a meaningful business, chronological, or process order when sorting would destroy the story.

## 5. Visual system

Use the supplied brand system first. Otherwise start with:

- Background: white or transparent.
- Primary text and axes: `#1F2937`.
- Secondary text and gridlines: `#6B7280` and `#D1D5DB`.
- Neutral data marks: `#CBD2DC` and `#8E99A8`.
- One primary accent: `#2F5DA8`.
- Optional positive and negative accents: `#2E7D32` and `#B3261E`, used sparingly.

Apply color semantically:

- Keep context series neutral and use one accent for the focus series, period, or driver.
- Preserve the same color meaning throughout a slide or deck.
- Do not assign a different saturated color to every category by default.
- Do not rely on red versus green alone. Add signs, labels, position, or patterns when the distinction matters.
- Avoid gradients, three-dimensional effects, drop shadows, glossy fills, and decorative borders.

## 6. Density and typography

- Prefer a compact plot with direct labels over a large empty plot surrounded by legends and separate callout boxes.
- Keep enough whitespace around the title, plot, and source to preserve grouping.
- Use the presentation theme font. Without a template, use a widely available sans serif font.
- Follow the destination artifact's typography guidance. For a presentation, keep chart labels readable when projected and avoid text below 17 pt unless the chart density makes a smaller size unavoidable and the rendered result remains legible.
- Make totals, endpoints, or the main comparison slightly stronger through weight or accent. Do not bold every label.

## 7. Source and caveats

- Preserve the unit, time range, geography, scenario, and source needed to interpret the data.
- Put a concise source line below the chart when the source is known.
- Put material qualifications near the affected title or annotation. Do not bury a caveat that changes the conclusion in tiny text.
