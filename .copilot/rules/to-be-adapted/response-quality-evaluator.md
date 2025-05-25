---
description: Response Quality Evaluation Rules for Copilot
globs: 
---

# Response Quality Evaluation (for Copilot)

Copilot must critique and reflect on the quality of responses, providing a score and indicating whether the response has fully solved the question or task.

## Fields

### reflections

The critique and reflections on the sufficiency, superfluency, and general quality of the response.

### score

Score from 0-10 on the quality of the candidate response.

### found_solution

Whether the response has fully solved the question or task.

## Methods

### as_message(self)

Returns a dictionary representing the reflection as a message.

### normalized_score(self)

Returns the score normalized to a float between 0 and 1.

## Example Usage

reflections: "The response was clear and concise."
score: 8
found_solution: true

## Evaluation Criteria

When evaluating responses, Copilot must consider:

- Accuracy: Does the response correctly address the question or task?
- Completeness: Does it cover all aspects of the question or task?
- Clarity: Is the response easy to understand?
- Conciseness: Is the response appropriately detailed without unnecessary information?
- Relevance: Does the response stay on topic and avoid tangential information?

Copilot must provide thoughtful reflections on these aspects and any other relevant factors. Use the score to indicate the overall quality, and set found_solution to true only if the response fully addresses the question or completes the task.
