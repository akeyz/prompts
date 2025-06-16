---
description: Defines a set of workflow stages for The AI assistants to transform vague ideas into a clear implementation plan, iteratively refining a single Markdown document.
tags: [workflow, planning, requirements, tasks, design, test-cases, llm, agent]
applyTo: ["*"]
compatibility: [Copilot, Cline, Roo Code, Any AI agent]
---

# Idea to implementation plan

Define a set of workflow stages for The AI assistants to transform vague ideas into a clear implementation plan, iteratively refining a single Markdown document.

## Workflow Initialization

1. User provides initial idea as input to the The AI assistant.
2. The AI assistant creates a new markdown file with the idea content under the `## Idea` heading. New markdown file name should reflect the idea.
3. The AI assistant confirms the initial idea is captured correctly before proceeding.

### Markdown File Creation Location

When creating a new planning markdown file, the AI assistant MUST follow this universal process:

1. Attempt to create the file in the project root directory.
2. If the root directory is not writable, recursively search for the first subdirectory with write permissions and create the file there.
3. If no writable location is found, the AI assistant MUST prompt the user to specify a directory before proceeding.

This ensures the workflow is robust and portable across all project types and environments.

## Core Interaction Model

This workflow enforces a strict "pause-ask-refine-continue" model for the AI assistant:

1. At each stage, the AI assistant MUST update only one section of the `.md` file (e.g., Idea, Requirements, Tasks, Design, Test Cases, Next Steps).
2. After each update, the AI assistant MUST pause and explicitly ask the user to review and confirm the changes for that section.
3. Only after receiving explicit user agreement can the AI assistant proceed to the next stage and update the next section.
4. If the user disagrees, the AI assistant MUST ask for specific feedback and refine the section accordingly, up to three cycles. If agreement is not reached after three refinements, the AI assistant MUST record the user's reservations in the `.md` file and suggest moving forward.
5. If the user requests to skip steps or output all sections at once, the AI assistant MUST warn that this may reduce quality, ask for explicit confirmation, and, if the user insists, record this override and rationale in the `.md` file.
6. All content MUST be written to the `.md` file, not just output as text.
7. The AI assistant MUST always wait for explicit user confirmation before continuing to the next stage.

This model ensures clarity, user control, and high-quality, stepwise refinement.

## Markdown File Structure

The AI assistant manages a single `.md` file with these H2 headings:

- `## Idea`
- `## Requirements`
- `## Tasks`
- `## Design`
- `## Test Cases`
- `## Next Steps`

## Workflow Stages

### 1. Idea to Requirements

- **Input**: User-provided idea.
- **Output**: Clear requirements with Given-When-Then acceptance criteria in `## Requirements`.
- **Process**:
  - Analyze idea content.
  - Ask clarifying questions (both yes/no and targeted open questions when necessary).
  - Draft requirements based on understanding.
  - Apply Core Interaction Model.

**This stage should follow guidelines from:**

- `[workflow-and-task-splitting.md]` for requirement analysis and decomposition.
- `[response-and-prompt-guidelines.md]` for user interaction.

### 2. Requirements to Tasks

- **Input**: Approved `## Requirements` section.
- **Output**: Granular, actionable tasks in `## Tasks`.
- **Process**:
  - Analyze requirements systematically.
  - Break down into MECE (Mutually Exclusive, Collectively Exhaustive) tasks.
  - Apply Core Interaction Model.

**This stage should follow guidelines from:**

- `[workflow-and-task-splitting.md]` for task breakdown.

### 3. Tasks to Design

- **Input**: Approved `## Tasks` section.
- **Output**: Design specifications with class/method structures and Mermaid diagrams in `## Design`.
- **Process**:
  - Analyze tasks.
  - Check for existing code context. Either in open tabs, or by searching the codebase.
  - Design components with consideration for existing systems.
  - Verify design completeness against tasks.
  - Apply Core Interaction Model.

**This stage should follow guidelines from:**

- `[programming-workflow.md]` for overall design process.
- `[code-standards.md]` and `[avoid-bad-smells.md]` for design and code quality.

### 4. Design to Test Cases

- **Input**: Approved `## Design` section.
- **Output**: Test scenarios in `## Test Cases`.
- **Process**:
  - Analyze design components.
  - Define positive, negative, and edge case tests.
  - Verify test coverage is complete.
  - Apply Core Interaction Model.
  - Add implementation recommendations to `## Next Steps` section.

**This stage should follow guidelines from:**

- `[testing-guidelines.md]` for test case design.
- `[programming-workflow.md]` for integrating testing into the workflow.
