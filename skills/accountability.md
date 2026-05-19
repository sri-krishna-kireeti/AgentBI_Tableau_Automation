# Accountability Skill (Governance)

## Description
Handles explainability, traceability, and proof generation for agent decisions. Always loaded in full (governance exclusion).

## Responsibilities
- explain KPI generation
- explain chart selection
- explain validation outcomes
- provide evidence references
- answer user challenges

## Required Evidence
- source columns
- transformation logic
- derivation logic
- validation results
- rejected alternatives

## Output Rules
Every major decision must include:
- why chosen
- evidence used
- alternatives rejected

## Storage
Write detailed execution evidence into:
- evidence/execution_logs/
- evidence/decision_logs/
- evidence/validation_reports/

# Learning Rules
Append new rules below this section only if they improve:
- accountability rules
- explainability
- traceability
- evidence storage
- user challenge handling