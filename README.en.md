[中文版](README.md)

# AI Agent Instruction Framework

## Overview

This repository hosts a comprehensive suite of system instructions meticulously crafted to direct AI agents (such as GitHub Copilot, Cline, Roo Code, and similar platforms) in executing complex software development tasks. The framework emphasizes precision, adherence to quality standards, and a methodical, disciplined approach to development.

These instructions are designed to augment the capabilities of AI agents by enforcing established best practices in software engineering, including coding standards, design principles, testing methodologies, workflow management, and effective human-AI collaboration.

## Who Can Benefit?

This framework is beneficial for:

*   **Developers** utilizing or constructing AI-assisted coding tools and seeking to standardize AI behavior.
*   **Teams** aiming to integrate AI agents into their software development lifecycle with consistent and high-quality outputs.
*   **Researchers and Engineers** focused on enhancing the reliability, quality, and predictability of AI-generated code and development processes.
*   **Business Analysts and Product Owners** collaborating with AI agents for requirements elicitation and user story generation.

## Instruction Modules

The instructions are organized into several key modules, mirroring the structure outlined in `[.github/instructions/overview.md](.github/instructions/overview.md)`:

*   **Core Behavior Definition:** Foundational principles governing agent operations and interaction.
*   **Standards & Quality Specifications:** Guardrails ensuring excellence in all generated artifacts and processes.
*   **Process Templates:** Systematic workflows for transforming concepts into implementable solutions.
*   **Tool Usage Guides:** Guidelines for leveraging specialized (potentially hypothetical) tools to accelerate complex cognitive tasks.

## Detailed File Descriptions

Below is a description of each instruction file located in the `[.github/instructions/](.github/instructions/)` directory:

### General Overview
*   `[.github/instructions/overview.md](.github/instructions/overview.md)`: Provides a high-level strategic overview of all instruction modules, their purpose, and how they integrate to form a cohesive framework for AI agent behavior.

### Core Behavior Definition
*   `[.github/instructions/memory-bank.instructions.md](.github/instructions/memory-bank.instructions.md)`: Details the "Memory Bank" system, a crucial component for AI agents to maintain project knowledge and context across sessions. It outlines the structure of memory files (e.g., `projectbrief.md`, `activeContext.md`) and defines workflows for their utilization and updates.
*   `[.github/instructions/response-and-prompt-guidelines.md](.github/instructions/response-and-prompt-guidelines.md)`: Specifies structured interaction protocols for AI agents, including response formatting (e.g., a mandatory 8-section structure), language conventions (e.g., Chinese for user explanations, English for technical terms), and core operational principles like clarity and critical skepticism.
*   `[.github/instructions/programming-workflow.md](.github/instructions/programming-workflow.md)`: Lays out a comprehensive, Test-Driven Development (TDD) oriented lifecycle for AI agents. This workflow covers phases from preparation and understanding (including Memory Bank consultation) through design, test implementation, coding, and refactoring, to final review.
*   `[.github/instructions/workflow-and-task-splitting.md](.github/instructions/workflow-and-task-splitting.md)`: Describes core principles (MECE, clear objectives, manageable size, prioritization, independence, verifiability) and a systematic process for decomposing complex requirements into smaller, actionable, and verifiable subtasks.

### Standards & Quality Specifications
*   `[.github/instructions/code-standards.md](.github/instructions/code-standards.md)`: Defines standards for clean code and overall code quality. It covers naming conventions, the Single Responsibility Principle (SRP), DRY (Don't Repeat Yourself), SOLID principles, OWASP security guidelines, and best practices for class/method design, database interactions, DevOps, and specific technology stacks (e.g., Java/Spring Boot).
*   `[.github/instructions/avoid-bad-smells.md](.github/instructions/avoid-bad-smells.md)`: Lists common code smells (e.g., duplicate code, long methods, feature envy, magic numbers, excessive comments) and anti-patterns (e.g., input kludges, interface bloat, anemic domain models, god objects) that AI agents must proactively identify and strictly avoid.
*   `[.github/instructions/testing-guidelines.md](.github/instructions/testing-guidelines.md)`: Provides comprehensive guidelines for designing and implementing high-quality tests. It includes principles for test clarity and independence, coverage of positive/negative/edge scenarios, a recommended test case template, and best practices for assertions.

### Process Templates
*   `[.github/instructions/req.md](.github/instructions/req.md)`: Outlines a structured workflow for transforming vague ideas into concrete and actionable implementation plans. This process involves iteratively refining a single Markdown document through stages: Idea, Requirements (with Gherkin-style acceptance criteria), Tasks, Design (including Mermaid diagrams), and Test Cases, all managed via a "pause-ask-refine-continue" interaction model.
*   `[.github/instructions/ba.md](.github/instructions/ba.md)`: Equips AI assistants with a strategic framework to support Business Analysts (BAs) in crafting high-quality agile artifacts. It focuses on transforming epics into focused user stories with precise acceptance criteria, using a disciplined "pause-ask-refine-continue" protocol for AI-BA collaboration and structured document management.

### Tool Usage Guides
*   `[.github/instructions/sequential-thinking.md](.github/instructions/sequential-thinking.md)`: Guides AI agents on the effective use of a hypothetical `sequentialthinking` MCP (Multi-Cognitive Process) tool. This tool is envisioned for dynamic and reflective problem-solving, enabling complex problem decomposition, iterative planning, and hypothesis-driven reasoning.
*   `[.github/instructions/shortcut-system-instruction.md](.github/instructions/shortcut-system-instruction.md)`: Defines how AI agents should recognize and execute user-defined shortcut commands (e.g., `plan!`, `d!`, `t!`, `m!`, `me!`). These shortcuts trigger specific, pre-defined workflows for various development tasks, enhancing operational efficiency.

## How to Use

These instructions are primarily intended to be used as system prompts or guiding documents for advanced AI agents involved in software development. Developers and teams can:

*   Integrate these instructions into their AI interaction frameworks.
*   Use them as a reference for crafting effective prompts for AI assistants.
*   Adapt and extend them to suit specific project needs and AI capabilities.

By adhering to this framework, AI agents can produce more reliable, maintainable, and high-quality software, while collaborating more effectively with human developers and stakeholders.
