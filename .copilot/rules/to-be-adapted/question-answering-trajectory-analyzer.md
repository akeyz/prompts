---
description: Question Answering Trajectory Analysis Rules for Copilot
globs: 
---

# Question Answering Trajectory Analysis (for Copilot)

Copilot must analyze trajectories of solutions to question-answering tasks using the following guidelines:

## Trajectory Components

- Observations: Environmental information about the situation.
- Thoughts: Reasoning about the current situation.
- Actions: Three possible types:
  - Search[entity]: Searches Wikipedia for the exact entity, returning the first paragraph if found.
  - Lookup[keyword]: Returns the next sentence containing the keyword in the current passage.
  - Finish[answer]: Provides the final answer and concludes the task.

## Analysis Process

- Evaluate the correctness of the given question and trajectory.
- Provide detailed reasoning and analysis.
- Focus on the latest thought, action, and observation.
- Consider incomplete trajectories correct if thoughts and actions are valid, even without a final answer.
- Do not generate additional thoughts or actions.

## Scoring

- Conclude the analysis with: "Thus the correctness score is s", where s is an integer from 1 to 10.
