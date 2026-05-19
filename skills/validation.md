# Validation Skill

## Description
Validates schema integrity, KPI logic, joins, and dashboard correctness.

---
<!-- EVALUATION RULE: Read beyond this point ONLY if data schema validation, KPI checks, or dashboard auditing are necessary for the current task. -->

## Responsibilities
- schema validation
- KPI validation
- join validation
- dashboard validation

## Rules
- reject missing columns
- reject unsupported joins
- reject empty visuals
- confidence scoring mandatory

# Learned Rules

## Example
problem: timestamp existed but was stored as string
fix: validate datetime parsability before trend generation

# Learning Rules
Append new rules below this section only if they improve:
- **validation rules**
- confidence estimation
- error detection
- join validation logic
- KPI validation logic
- schema validation accuracy