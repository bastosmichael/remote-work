# Overview of Agents in This Repository

This document outlines the LLM-based and autonomous agents used in this project. It provides detailed information on their roles, triggers, behaviors, and outputs, serving as a reference for contributors and AI tooling.

## Table of Agents

| Name         | Description                                      | Trigger                                                    |
|--------------|--------------------------------------------------|-----------------------------------------------------------|
| Doc Writer   | Generates and updates README.md files automatically based on project structure. | Triggered by file changes in the repository.              |
| Test Case Generator | Creates unit tests based on function signatures and comments. | Triggered by pull requests with new features.             |
| CI Workflow Creator | Automates the creation of Continuous Integration workflows. | Triggered when new push events occur in the main branch.  |

### Agent 1: Doc Writer

**Name**: Doc Writer

**Description**: The Doc Writer agent generates and updates README.md files automatically based on the current project structure and contents.

**Trigger**: Triggered by file changes in the repository.

**Inputs and Outputs**:
- **Inputs**: Project structure, existing README.md content.
- **Outputs**: Updated README.md file.

**Logic Location**: `/agents/doc-writer.ts`

**Review or Audit Process**: The generated README is reviewed by the documentation team before merging into the main branch.

### Agent 2: Test Case Generator

**Name**: Test Case Generator

**Description**: This agent creates unit tests based on function signatures and comments within the code.

**Trigger**: Triggered by pull requests that introduce new features or functions.

**Inputs and Outputs**:
- **Inputs**: Function signatures, comments.
- **Outputs**: Generated test files.

**Logic Location**: `/agents/test-case-generator.ts`

**Review or Audit Process**: Generated test cases are evaluated during code reviews.

### Agent 3: CI Workflow Creator

**Name**: CI Workflow Creator

**Description**: Automates the process of creating Continuous Integration workflows to streamline deployment and testing.

**Trigger**: Triggered when new push events occur in the main branch.

**Inputs and Outputs**:
- **Inputs**: Code changes, configuration settings.
- **Outputs**: CI workflow files.

**Logic Location**: `/agents/ci-workflow-creator.ts`

**Review or Audit Process**: CI workflows are reviewed as part of the pull request process.

## How to Invoke Each Agent

### Agent 1
- **CLI**: `npm run generate-docs`
- **CI**: Automatically triggered on new pull requests to the repository.

### Agent 2
- **CLI**: `npm run generate-tests`
- **CI**: Activated on new feature pull requests.

### Agent 3
- **CLI**: `npm run create-ci-workflow`
- **CI**: Activated on changes to specific configuration files in the repository.

## Future Agent Proposals

### Proposed Agent 4: Dependency Updater
- **Functionality**: Automatically updates project dependencies based on the latest compatible versions.
- **Trigger**: Scheduled daily checks.
- **Expected Benefits**: Keep dependencies current and secure without manual intervention.

## Contribution Instructions for New Agents

To propose or implement a new agent, follow these steps:
1. **Proposal**: Open an issue with the `agent-proposal` label, detailing the agent's functionality, triggers, and expected benefits.
2. **Implementation**: Once approved, implement the agent in the appropriate directory and update this document with the new agent's details.
3. **Review**: Submit a pull request for review, ensuring the agent's documentation is included in `AGENTS.md`.
