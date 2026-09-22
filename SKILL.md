---
name: professional-charts
description: Create, edit, or critique decision-ready business charts. Use for professional, consulting-style, or management charts, especially waterfall, Mekko, Gantt, variance, CAGR, directly labeled, or insight-led charts. Do not use for PowerPoint or presentation generation, or for decorative infographics with no quantitative chart.
---

# Professional charts

Create decision-ready charts whose business meaning is visible in the final artifact. Apply a professional business-chart visual grammar independent of the tool or file format used to create it.

## Route the request

1. Determine the data, comparison being made, and desired takeaway.
2. Honor the user's requested output format and active workspace. Do not assume a presentation platform, cloud service, or creation tool when none is specified.
3. If no format is specified, create a high-resolution PNG or SVG chart rather than a presentation file. When raster dimensions are otherwise unknown, use at least 1600 px width or export at 2× the intended logical layout size.
4. For an existing artifact or brand template, preserve its theme, fonts, margins, and established color meanings before applying the defaults in this skill.
5. Do not use image generation for quantitative marks, labels, or annotations. Generate them from the supplied data so that every visible value is auditable.

## Before drawing

- Read [visual grammar](references/visual-grammar.md) for every creation, edit, or critique task.
- Read only the relevant sections of [chart recipes](references/chart-recipes.md) after selecting the chart family.
- Inspect the data before choosing the chart. Confirm units, time periods, category order, missing values, signs, totals, and whether percentages use a common denominator.
- Use the most specific business metric name supported by the supplied data or confirmed context. Do not expand an acronym, add a metric definition, or infer an underlying business mechanism without evidence.
- Identify the single comparison or conclusion the chart must make easy to see. If the evidence does not support a conclusion, use a factual topic title and show the data without inventing a takeaway.
- For an event, launch, intervention, or policy marker, define the comparison interval before writing the annotation. Recalculate the change from the endpoints named by the claim, and do not present temporal alignment as causal proof.
- Treat claims such as acceleration, slowdown, steeper growth, or significant improvement as derived findings. Compare like-for-like rates over explicit intervals, distinguish a one-period level shift from a sustained slope change, and reserve “statistically significant” for a supported statistical test.
- Calculate derived values before layout: totals, subtotals, shares, absolute differences, relative differences, and CAGR. Follow the formula and edge-case rules in the visual grammar reference.

## Choose the chart by the analytical question

- Compare categories or rankings: horizontal bar or column.
- Show composition: stacked bar or 100% stacked bar.
- Explain change from a starting value to an ending value: waterfall.
- Show a trend: line; use area only when the changing total or composition matters.
- Combine level and trend: combination chart, with a second axis only when units genuinely differ.
- Show the relationship between two or three variables: scatter or bubble.
- Show total market size and internal share together: Mekko.
- Show a simple part-to-whole with few categories: pie or doughnut.
- Show schedule, phases, milestones, or dependencies: Gantt.

Prefer the simplest chart that carries the intended comparison. Do not use Mekko, bubble, dual-axis, or pie charts merely for visual novelty.

## Build the artifact

- Use chart objects or vector shapes supported by the requested destination format.
- Do not create or edit PowerPoint files as part of this skill. If the user explicitly requests a presentation, explain that this skill produces chart assets and use the appropriate presentation workflow separately only when requested.
- Derive the position and dimensions of every data-bearing shape from shared plot bounds and scales. Do not place bars, lines, arrows, or labels by eye.
- Keep title, chart marks, annotations, source note, and any legend as separate editable objects.
- Use direct labels by default. Keep a legend only when direct labeling would make the chart less readable.
- Treat CAGR arrows, difference arrows, total/subtotal bars, value lines, forecast separators, and axis breaks as data-bearing elements. Position them according to the data scale, not by eye.
- If synthetic data is requested for an example, label it clearly as example data. Never mix synthetic values with supplied real data without disclosure.

## Validate and deliver

Read and apply [quality gates](references/quality-gates.md) before delivery.

Render or export a preview in the requested format. Inspect the final chart at full size and correct overlaps, clipped labels, misleading scales, weak contrast, excessive decimals, and ambiguous annotations before delivery.

When reporting the result, state the chart type, the main encoded comparison, and any limitation that affects interpretation.
