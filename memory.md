Title: Global Memory
Description: Stores orchestration and workflow learnings. Always loaded in full (core orchestration exclusion).
Must stay lightweight.

---

# Learned Optimizations

## Workflow
- validate schema before dashboard planning
- block visualization generation if KPI invalid

## Token Optimization
- avoid repeated schema scans
- load only required skills

## Execution
- validate visuals before packaging output
- **CRITICAL**: When generating `.twb` XML entirely from scratch, you MUST include a `<windows>` block at the end of the XML before `</workbook>`. Omitting the `<windows>` block will result in a fatal Internal Error 501CF476.
- Worksheets must include `<simple-id uuid='{...}' />` after `<table>`.
- Dashboard zones must use `param='Worksheet Name'` (not the datasource prefix) and `type-v2='worksheet'` (since `type='worksheet'` throws an enumeration error).
- Tableau calculations must use a single `=` for equality, not `==`.
- Line charts should only be used for true temporal data. Use Bar charts for categorical comparisons to avoid internal layout errors.

# Learning Rules
Append new rules below this section only if they improve:
- auditability
- accountability
- workflow improvements
- token optimization
- execution improvements

## Visualization Generation
- **Aesthetics**: Never rely on generic Tableau defaults. Explicitly encode semantic color palettes and data labels directly in the `.twb` XML.
- **Aggregation**: Map ordinal/survey data to aggregated bar charts (using `avg` or `cnt`), strictly avoiding unreadable dense scatter plots.
- **Stability**: Generating `.twb` XML from scratch is permitted and succeeds ONLY IF the file structurally concludes with a properly mapped `<windows>` block to prevent 501CF476 layout engine crashes.