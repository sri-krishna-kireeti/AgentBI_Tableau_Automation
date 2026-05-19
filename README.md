# TableauAI

An enterprise BI Engineering Agent project designed to automate and assist with Tableau reporting.

## Overview
This project contains the logic, skills, and templates for a Tableau Reporting Agent, which is responsible for:
- Understanding reporting requirements
- Analyzing enterprise documents and reports
- Reusing governed business logic
- Generating traceable BI artifacts (e.g., `.twb` files)
- Maintaining report lifecycle governance
- Ensuring explainability and auditability

## Directory Structure
- `documents/`: Contains enterprise documents and reference materials.
- `evidence/`: Stores execution and decision logs for auditability.
- `skills/`: Contains the agent's modular skill files.
- `user_requirements/`: Stores the user's reporting requirements.
- `gemini.md`, `memory.md`, `security.md`: Core configuration and memory files for the agent.

## Usage
This repository is intended to be used with the agentic setup described in the core `.md` files. Simply clone the repository and configure your agent to point to this directory to utilize the enterprise BI workflows.
