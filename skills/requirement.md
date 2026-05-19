# Requirement Skill

## Description
Transforms BA/business requests into structured dashboard implementation plans.

---
<!-- EVALUATION RULE: Read beyond this point ONLY if requirement analysis or plan generation is necessary for the current task. -->

## Responsibilities
- identify KPIs
- identify visuals
- identify filters
- identify datasets
- identify missing requirements

## Rules
- every KPI requires a visual
- every visual requires mapped fields
- ambiguous logic => clarification required
- If business thresholds are missing but required for KPI generation, the agent may propose statistically reasonable defaults labeled as 'Suggested Logic' and require explicit approval before execution.

# Learned Rules

## Example
problem: business requested growth KPI without date field
fix: request time dimension clarification before planning

# Learning Rules
Append new rules below this section only if they improve:
- **requirement analysis rules**
- KPI identification accuracy
- layout and visual selection
- filter mapping accuracy
- ambiguity resolution rules