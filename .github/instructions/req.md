# Idea to implementation plan

Define a set of workflow functions for LLM/agents to transform vague ideas into a clear implementation plan, iteratively refining a single Markdown document.

## Core Interaction Model

The "pause-ask-refine-continue" model:

1. After each function completes an update to the `.md` file, the LLM/agent MUST pause.
2. It MUST ask the user to review the changes and confirm agreement.
3. If the user agrees, the LLM/agent proceeds to the next function in sequence.
4. If the user disagrees, the LLM/agent asks for specific points of disagreement and refines the relevant section until:
   - Agreement is reached, or
   - Three refinement cycles occur (then suggest moving forward with reservations noted).

## Workflow Initialization

1. User provides initial idea as input to the LLM/agent.
2. LLM/agent creates a new markdown file with the idea content under the `## Idea` heading. New markdown file name should reflect the idea.
3. LLM/agent confirms the initial idea is captured correctly before proceeding.

## Markdown File Structure

LLM/agent manages a single `.md` file with these H2 headings:

- `## Idea`
- `## Requirements`
- `## Tasks`
- `## Design`
- `## Test Cases`
- `## Next Steps`

## Workflow Functions

### 1. Idea to Requirements

- **Input**: User-provided idea in the `## Idea` section.
- **Output**: Clear requirements with Given-When-Then acceptance criteria in `## Requirements`.
- **Process**:
  - Analyze idea content.
  - Ask clarifying questions (both yes/no and targeted open questions when necessary).
  - Draft requirements based on understanding.
  - Apply Core Interaction Model.

### 2. Requirements to Tasks

- **Input**: Approved `## Requirements` section.
- **Output**: Granular, actionable tasks in `## Tasks`.
- **Process**:
  - Analyze requirements systematically.
  - Break down into MECE (Mutually Exclusive, Collectively Exhaustive) tasks.
  - Apply Core Interaction Model.

### 3. Tasks to Design

- **Input**: Approved `## Tasks` section.
- **Output**: Design specifications with class/method structures and Mermaid diagrams in `## Design`.
- **Process**:
  - Analyze tasks.
  - Check for existing code context. Either in open tabs, or by searching the codebase.
  - Design components with consideration for existing systems.
  - Verify design completeness against tasks.
  - Apply Core Interaction Model.

### 4. Design to Test Cases

- **Input**: Approved `## Design` section.
- **Output**: Test scenarios in `## Test Cases`.
- **Process**:
  - Analyze design components.
  - Define positive, negative, and edge case tests.
  - Verify test coverage is complete.
  - Apply Core Interaction Model.
  - Add implementation recommendations to `## Next Steps` section.
