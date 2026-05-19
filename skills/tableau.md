# Tableau Skill

## Description
Generates Tableau dashboards and visual layouts.

---
<!-- EVALUATION RULE: Read beyond this point ONLY if Tableau visual selection, layout design, or workbook generation is necessary for the current task. -->

## Responsibilities
- dashboard generation
- chart selection
- visual layouts
- filters/interactions
- tableau packaging

## Rules
- visuals mandatory
- no KPI-only pages
- avoid duplicate visuals
- chart must match analytical intent

## Visual Mapping
trend=line
comparison=bar
distribution=histogram
correlation=scatter (WARNING: Avoid scatter plots for dense ordinal survey data like 1-10 scales. Aggregate to Bar charts instead).

# Learned Rules

## Example
problem: generated KPI cards without supporting trends
fix: add analytical chart for each KPI group

## Example
problem: overcrowded dashboard
fix: max 4 visuals/page unless explicitly requested

## Example
problem: Tableau throws Internal Error 501CF476 when generating `.twb` XML.
fix: Ensure all `<rows>`, `<cols>`, and `<encodings>` use strict Tableau "pill descriptors" that include the datasource prefix (e.g., `[datasource_name].[none:column_name:nk]`). Also, explicitly declare a `<column-instance>` for each inside `<datasource-dependencies>`. Dashboards must use `type-v2='worksheet'` and `param='[datasource_name].[worksheet_name]'` for zone mappings.

# Learning Rules
Append new rules below this section only if they improve:
- **Tableau-specific generation rules**
- chart selection accuracy
- layout efficiency
- filter effectiveness
- visualization best practices
- dashboard performance

## Example
problem: Visualizations generated as tiny slivers without values or aesthetic appeal.
fix: Always explicitly declare quantitative aggregations (e.g., `cnt`, `avg`) in the `<column-instance>` XML derivations. Inject custom `<style>` blocks for semantic color palettes and `<format attr='mark-labels-show' value='true' />` to guarantee executive readability out-of-the-box.
