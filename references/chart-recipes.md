# Chart recipes

Read the selection guidance and only the recipes relevant to the requested chart.

## Selection guide

| Analytical question | Default chart | Use another chart when |
| --- | --- | --- |
| Which category is larger? | Sorted horizontal bar | Time is the main dimension, then use columns or a line |
| How is a total composed? | Stacked or 100% stacked bar | Total size and share both matter, then consider Mekko |
| What caused the change? | Waterfall | Only the start and end trend matter, then use a line or two columns |
| How did values evolve? | Line | Composition over time matters, then use area |
| Are two variables related? | Scatter | A third size variable matters, then use bubble |
| What is the project schedule? | Gantt | Only a few dated events matter, then use a simple timeline |

## Column and bar

Use for precise length comparisons.

- Prefer horizontal bars for long category names or rankings.
- Use columns for short categories, periods, or stage comparisons.
- Use clustered bars only when each series needs direct comparison at each category.
- Use stacked bars for totals plus composition; use 100% stacks only when share is the message.
- Label important segments and totals directly. Remove redundant axes when every bar is labeled.
- Create intentional category gaps to separate historical and forecast periods or logical groups.
- For a butterfly chart, place two horizontal bar plots back to back, use the same scale, and keep category labels on the shared center line.

Avoid more than two or three clustered series when the values become difficult to compare.

## Waterfall

Use when components reconcile a start value to an end value.

Represent each item as one of four semantic types:

- `start`: total from zero to the starting value.
- `delta`: floating bar from the previous cumulative value to the new cumulative value.
- `subtotal`: total from zero to the cumulative value at that point.
- `total`: final total from zero to the ending value.

For each delta `d` with previous cumulative value `p`:

- next cumulative value: `q = p + d`
- bar lower edge: `min(p, q)`
- bar upper edge: `max(p, q)`
- connector level after the bar: `q`

Design rules:

- Distinguish totals from drivers through fill, outline, or weight.
- Use signs and data labels. Do not make color the only positive/negative cue.
- Draw thin connectors to preserve the bridge logic.
- When showing the net change from the starting total to the ending total, reserve an annotation column to the right of the ending total. Extend a horizontal dashed guide from the outer top edge of each total to that column, join the two guide levels with a vertical double-ended arrow, and place the absolute difference plus any valid relative difference beside the arrow.
- Keep the total-value labels clear of these guides. Do not raise a vertical comparison line from the center of either total bar because it can pass through the endpoint value. The vertical difference arrow belongs only in the separate annotation column; move the label or reserve more margin if the required clearance is unavailable.
- Do not represent the start-to-end net change with a curved, arcing, or dotted line over the intermediate drivers. The net-change annotation compares the two total endpoints; it is not a trend path.
- Keep subtotal and total columns on the baseline.
- Allow a delta to cross zero when the data requires it.
- Use a horizontal waterfall only when category labels or slide geometry clearly benefit.

Verify that the final cumulative value reconciles exactly with the shown total, subject only to disclosed rounding.

## Line, area, and combination

Use a line for trends and an area chart for changing totals or composition.

- Label line endpoints directly when possible.
- Highlight one focal series and keep comparison series neutral.
- Use markers only when individual observations matter or the series is sparse.
- Show missing values honestly. Do not interpolate across a meaningful data gap without disclosure.
- Use a value line for targets and a separator for actual versus forecast periods.
- Use a CAGR arrow only across valid positive endpoints and elapsed periods.
- In an area chart, order series so important or stable components remain readable.

For a combination chart, use columns for magnitude and a line for a rate, index, or reference series. Add a second axis only when the units differ and a common scale cannot express the comparison honestly.

## Mekko

Use a percentage Mekko when category size and within-category mix both matter.

For category `j` and segment `i`, with value `v[i,j]`:

- category total: `T[j] = sum_i v[i,j]`
- column width share: `T[j] / sum_j T[j]`
- segment height share: `v[i,j] / T[j]`
- segment area share: `v[i,j] / sum_j T[j]`

Construct columns without gaps so width comparisons remain valid. Label column totals or width shares and show segment shares selectively. Combine immaterial segments into a disclosed “Other” category when labels would become unreadable.

Use a unit-axis Mekko only when the user needs independently controlled column widths and absolute segment heights. Label both encodings explicitly because area no longer has the same part-to-whole meaning as in a percentage Mekko.

Avoid Mekko when audiences need precise comparison of similarly sized rectangles; use bars or a table instead.

## Scatter and bubble

Use scatter for relationship, clustering, or outliers. Use bubble only when the third variable changes the interpretation.

- Label notable points directly and de-emphasize the rest.
- State units on both axes.
- Add quadrant lines only when thresholds have business meaning.
- Add a trend line only when analytically justified; do not imply causation from correlation.
- Map bubble size to area and include a size reference if magnitude is not obvious.
- Use transparency when marks overlap.

## Pie and doughnut

Use only for a simple part-to-whole with one series and few categories.

- Sort slices or preserve a meaningful conventional order.
- Start the first important boundary at 12 o'clock when practical.
- Directly label slices with category and share.
- Emphasize at most one slice.
- Prefer a bar chart when categories are numerous or values are close.
- Do not use concentric rings unless each ring has the same categories and the comparison remains legible.

## Gantt

Use a calendar-aligned grid with activity rows.

- Choose the coarsest calendar scale that still supports the planning decision: day, week, month, quarter, or year.
- Use bars for duration, diamonds for milestones, brackets for phases, vertical lines for cross-project milestones, and light shading for blocked or non-working periods.
- Align every mark to an actual date. Do not position milestones by eye.
- Keep activity names close to their rows. Add owner, status, or progress columns only when the audience needs them.
- Use consistent status colors and include text or symbols so the chart does not depend on color alone.
- Show dependencies only when they affect the critical reading of the schedule. Excessive connectors obscure the plan.

## Native objects versus editable shapes

- Prefer a native chart when standard chart semantics and ordinary labels are sufficient.
- Prefer editable shapes for advanced waterfall bridges, Mekko geometry, Gantt items, custom difference/CAGR arrows, and deliberate axis breaks.
- When using shapes, derive every position from the same plot bounds and scale mapping. Do not eyeball bar heights or annotation anchors.
- Group related marks only when grouping does not prevent later editing.
