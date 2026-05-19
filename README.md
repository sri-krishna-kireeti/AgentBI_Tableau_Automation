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

## Example output by the Agent
<img width="1913" height="1022" alt="image" src="https://github.com/user-attachments/assets/2dbfdbbf-0fbb-4f5b-8a21-3d77eee3158c" />

## How to Use TableauAI
1. **Add Reference Documents**: Place all the reference tables, data dictionaries, and context files into the `documents/` folder.
2. **Add Requirements**: Place your raw business requirements into the `user_requirements/` folder. There's no need to manually structure or format them—the agent will handle that.
3. **Review and Approve**: The agent will automatically analyze the requirements and propose a structured logical plan. Review the structure and logic provided by the agent. If it looks correct, you can approve it and ask the agent to proceed with generating the Tableau report.
4. **Note on Stability**: I am continuously working on adding stricter Tableau rules and logic constraints to ensure the generated reports do not break when opened in Tableau.

## Usage
This repository is intended to be used with the agentic setup described in the core `.md` files. Simply clone the repository and configure your agent to point to this directory to utilize the enterprise BI workflows.
