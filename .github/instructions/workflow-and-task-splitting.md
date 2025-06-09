---
description: Workflow and task splitting guidelines for AI assistants and developers.
tags: workflow, task-splitting, ai-guidelines
applyTo: *
compatibility: Copilot, Cline, Roo Code, Any AI agent
---

# Workflow & Task Splitting

## Programming Workflow for AI Assistants

This workflow applies to Copilot, Cline, Roo Code, or any AI assistant (and developers) handling any software programming task.

1. Understand the technical requirements, including the concepts involved and their relationships.
2. Split the requirement into mutually exclusive and collectively exhaustive components.
3. Convert the requirement into a technical design and list the tasks needed to implement the design.
4. For each task, design verification approaches such as test cases.
5. For each verification approach, define the classes and methods needed to implement those verifications.
6. The design should include the relationships between these classes and methods.
7. Only in the final step should you implement the classes and methods. Implementation must always be the last step.

## Task Splitting

- Always split tasks into MECE (mutually exclusive, collectively exhaustive) subtasks with clear goals and deliverables.
- Prioritize business value and implementation order.
- Briefly explain the splitting approach, then list subtasks in order.
