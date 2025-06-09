# Instruction Files Relationship Diagram

This document contains a Mermaid diagram illustrating the relationships and dependencies between the various instruction Markdown files located in the `.github/instructions/` directory.

## Diagram

```mermaid
graph TD
    subgraph "📚 Foundational Quality & Standards"
        CS["code-standards.md"]
        ABS["avoid-bad-smells.md"]
    end

    subgraph "⚙️ Development Workflow & Process"
        PW["programming-workflow.md"]
        WTS["workflow-and-task-splitting.md (Task Splitting Principles)"]
        TG["testing-guidelines.md"]
        MB["memory-bank.instructions.md"]
    end

    subgraph "🤖 AI Interaction & Specific Tools"
        RPG["response-and-prompt-guidelines.md"]
        SSI["shortcut-system-instruction.md"]
        ST["sequential-thinking.md"]
    end

    %% Core Dependencies & References
    PW --> CS
    PW --> ABS
    PW --> TG
    PW --> MB
    PW --> WTS

    ABS --> CS

    RPG --> ST
    RPG --> SSI
    RPG --> MB

    %% Shortcut System Instruction (SSI) references many other documents for its commands.
    %% For clarity, its broad references are described textually rather than cluttering the diagram.
    %% Specific command references within SSI point to: PW, WTS, RPG, CS, ABS, TG, MB, and SSI itself.

    classDef default fill:#f9f9f9,stroke:#333,stroke-width:2px,color:#333;
    classDef subgraphDef fill:#ececff,stroke:#9370db,stroke-width:2px,color:#333,font-weight:bold;

    class CS,ABS subgraphDef;
    class PW,WTS,TG,MB subgraphDef;
    class RPG,SSI,ST subgraphDef;
```

## Diagram Explanation

*   **Boxes**: Represent each instruction Markdown file.
*   **Subgraphs**: Group files by their core functional domain:
    *   `Foundational Quality & Standards`: Contains basic standards for coding and quality.
    *   `Development Workflow & Process`: Includes guidelines for the development lifecycle, task management, and testing.
    *   `AI Interaction & Specific Tools`: Covers AI response structure, shortcut commands, and guidelines for specific tools like the Memory Bank and Sequential Thinking.
*   **Solid Arrows (`-->`)**: Indicate a direct reference or strong logical dependency from one file to another. For example, `programming-workflow.md` (PW) references `code-standards.md` (CS).
*   **`shortcut-system-instruction.md` (SSI)**: This file references multiple other documents extensively based on the specific shortcut command being invoked. To maintain diagram clarity, its broad referential nature is noted in the diagram's comments rather than being fully depicted with arrows.

This diagram aims to provide a better understanding of how these instruction files interrelate and form a cohesive set of guidelines for The AI Assistant.