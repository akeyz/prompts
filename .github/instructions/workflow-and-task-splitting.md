---
description: Guidelines for effective task splitting for The AI Assistant and developers.
tags: task-splitting, planning, project-management, ai-guidelines
applyTo: ["*"]
compatibility: Copilot, Cline, Roo Code, Any AI agent
---

# Task Splitting Principles

*This document outlines task splitting principles for The AI Assistant (defined as Copilot, Cline, Roo Code, or any similar AI agent) and developers.*

Effective task splitting is crucial for managing complexity, ensuring clarity, and facilitating incremental progress. These principles should be applied when decomposing larger requirements or objectives.

Refer to [Unified Programming Workflow](./programming-workflow.md) for how task splitting fits into the broader development lifecycle.

## Core Task Splitting Principles

- **MECE Principle**: Tasks should be **M**utually **E**xclusive (no overlap in scope) and **C**ollectively **E**xhaustive (together they cover the entire requirement).
- **Clear Objectives & Deliverables**: Each subtask must have a precisely defined objective and an expected, verifiable deliverable.
- **Manageable Size**: Break tasks down into chunks that are small enough to be completed within a reasonable timeframe (e.g., a few hours to a day for significant subtasks, or smaller for micro-tasks within a development session). This aids in tracking progress and maintaining momentum.
- **Prioritization**:
    - Consider **business value**: Address high-value items earlier, if possible.
    - Consider **dependencies and logical order**: Implement foundational tasks before those that depend on them.
    - Consider **risk**: Tackle high-risk or uncertain tasks earlier to uncover potential issues sooner.
- **Independence (where possible)**: Aim for subtasks that can be worked on and tested independently to allow for parallel work or focused effort.
- **Verifiability**: Design subtasks so that their completion can be clearly verified (e.g., through specific tests, demonstrations, or a checklist of criteria).

## Process for Task Splitting

1.  **Understand the Overall Goal**: Ensure a clear understanding of the main requirement or problem to be solved.
2.  **Identify Major Components/Steps**: Break down the overall goal into its largest logical parts or sequential phases.
3.  **Decompose Further (Iterative)**: For each major component, assess if it's small and clear enough. If not, decompose it further using the MECE principle until all subtasks are manageable and meet the criteria above.
4.  **Define and Document**: For each subtask:
    -   Write a clear, concise description.
    -   State its specific objective(s).
    -   List its key deliverable(s).
    -   Note any dependencies on other tasks.
5.  **Review and Refine**: Review the complete list of subtasks to ensure they are collectively exhaustive, mutually exclusive, and logically sequenced. Adjust as necessary.
6.  **Communicate**: Briefly explain the task splitting approach (e.g., "The requirement was split by feature area, then by frontend/backend components") before listing the subtasks.
