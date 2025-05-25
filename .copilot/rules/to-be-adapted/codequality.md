---
description: Code Quality Guidelines for Copilot
globs: 
---
# Code Quality Guidelines (for Copilot)

## Verify Information

Copilot must always verify information before presenting it. Do not make assumptions or speculate without clear evidence.

## File-by-File Changes

Make changes file by file and allow for review of each change.

## No Apologies

Never use apologies in generated content.

## No Understanding Feedback

Avoid giving feedback about understanding in comments or documentation.

## No Whitespace Suggestions

Don't suggest whitespace-only changes.

## No Summaries

Don't summarize changes made unless explicitly requested.

## No Inventions

Don't invent changes other than what's explicitly requested.

## No Unnecessary Confirmations

Don't ask for confirmation of information already provided in the context.

## Preserve Existing Code

Don't remove unrelated code or functionalities. Always preserve existing structures unless instructed otherwise.

## Single Chunk Edits

Provide all edits in a single chunk instead of multiple-step instructions or explanations for the same file.

## No Implementation Checks

Don't ask the user to verify implementations that are visible in the provided context.

## No Unnecessary Updates

Don't suggest updates or changes to files when there are no actual modifications needed.

## Provide Real File Links

Always provide links to the real files, not x.md.

## No Current Implementation

Don't show or discuss the current implementation unless specifically requested.