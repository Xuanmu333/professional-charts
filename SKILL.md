---
name: professional-charts
description: Create, edit, or critique editable, decision-ready business charts directly in Google Slides. Use for professional, consulting-style, or management charts, especially waterfall, Mekko, Gantt, variance, CAGR, directly labeled, or insight-led charts. Do not use for decorative infographics with no quantitative chart.
---

# Professional charts

Create decision-ready charts whose business meaning is visible in the final artifact. Apply a professional business-chart visual grammar independent of the tool or file format used to create it.

## Route the request

1. Determine the data, comparison being made, and desired takeaway.
2. If the output format is unspecified or the user requests a presentation or slides, default to creating an editable Google Slides presentation with `workspace__create_presentation` and `workspace__batch_update_presentation`.
3. Build the chart as native shapes and text boxes inside the newly created Google Slide so every value, label, bar, line, and annotation is fully editable.
4. For an existing Google Slides deck or brand template, preserve its theme, fonts, margins, and established color meanings before applying the defaults in this skill.
5. Do not use image generation for quantitative marks, labels, or annotations. Generate them from the supplied data so that every visible value is auditable.

## Before drawing

- Read [visual grammar](references/visual-grammar.md) for every creation, edit, or critique task.
- Read only the relevant sections of [chart recipes](references/chart-recipes.md) after selecting the chart family.
- Inspect the data before choosing the chart. Confirm units, time periods, category order, missing values, signs, totals, and whether percentages use a common denominator.
- Identify the single comparison or conclusion the chart must make easy to see. If the evidence does not support a conclusion, use a factual topic title and show the data without inventing a takeaway.
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

- Create the online presentation in Google Drive with `workspace__create_presentation`, then construct or update the slide with `workspace__batch_update_presentation`.
- Use native Google Slides shapes, lines, and text boxes for every chart mark. Do not generate a local presentation file or use one as an import intermediary.
- Derive the position and dimensions of every data-bearing shape from shared plot bounds and scales. Do not place bars, lines, arrows, or labels by eye.
- Keep title, chart marks, annotations, source note, and any legend as separate editable objects.
- Use direct labels by default. Keep a legend only when direct labeling would make the chart less readable.
- Treat CAGR arrows, difference arrows, total/subtotal bars, value lines, forecast separators, and axis breaks as data-bearing elements. Position them according to the data scale, not by eye.
- If synthetic data is requested for an example, label it clearly as example data. Never mix synthetic values with supplied real data without disclosure.

## Validate and deliver

Read and apply [quality gates](references/quality-gates.md) before delivery.

1. Create the presentation in Google Drive.
2. Output the direct clickable Google Slides URL to the user.
3. Also provide a high-resolution PNG preview of the slide.

Inspect the PNG preview before delivery. Correct overlaps, clipped labels, misleading scales, weak contrast, excessive decimals, and ambiguous annotations in Google Slides, then regenerate the preview.

When reporting the result, state the chart type, the main encoded comparison, and any limitation that affects interpretation.
