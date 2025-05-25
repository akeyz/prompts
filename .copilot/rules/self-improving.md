---
description: Defines a process for Copilot to reflect on interactions and suggest improvements to active .copilot/rules. Copilot must follow these rules for self-improvement and rule refinement.
author: https://github.com/nickbaumann98
version: 1.0
tags: ["meta", "self-improvement", "reflection", "core-behavior", "copilot"]
globs: ["*"]
---

# Self-Improving Reflection (for Copilot)

**Objective:** Copilot must offer opportunities to continuously improve `.copilot/rules` based on user interactions and feedback.

**Trigger:** Before any task that involved user feedback provided at any point during the conversation, or involved multiple non-trivial steps (e.g., multiple file edits, complex logic generation), Copilot must follow this process.

**Process:**

1. **Offer Reflection:** Copilot must ask the user: "Before I complete the task, would you like me to reflect on our interaction and suggest potential improvements to the active `.copilot/rules`?"
2. **Await User Confirmation:** Copilot must proceed to `attempt_completion` immediately if the user declines or doesn't respond affirmatively.
3. **If User Confirms:**

    a.  **Review Interaction:** Copilot must synthesize all feedback provided by the user throughout the entire conversation history for the task. Analyze how this feedback relates to the active `.copilot/rules` and identify areas where modified instructions could have improved the outcome or better aligned with user preferences.

    b.  **Identify Active Rules:** Copilot must list the specific global and workspace `.copilot/rules` files active during the task.

    c.  **Formulate & Propose Improvements:** Copilot must generate specific, actionable suggestions for improving the *content* of the relevant active rule files. Prioritize suggestions directly addressing user feedback. Use `replace_in_file` diff blocks when practical, otherwise describe changes clearly.

    d.  **Await User Action on Suggestions:** Copilot must ask the user if they agree with the proposed improvements and if they'd like Copilot to apply them *now* using the appropriate tool (`replace_in_file` or `write_to_file`). Apply changes if approved, then proceed to `attempt_completion`.

**Constraint:** Do not offer reflection if:

* No `.copilot/rules` were active.
* The task was very simple and involved no feedback.
