# Prompt Improvement Command

Enhance user prompts through clarification, rewriting, structured output, and optimal persona selection for better AI assistance.

## Command

`/improve-prompt`

## Purpose

Transform ambiguous or unclear user requests into precise, actionable prompts that enable optimal AI assistance through systematic clarification and enhancement.

## Usage

```
/improve-prompt [mode] [focus]
```

**Modes:**
- `clarify` - Ask clarifying questions for ambiguous prompts
- `rewrite` - Improve prompt clarity and structure
- `optimize` - Enhance for specific AI persona and context
- `structure` - Apply structured response formatting
- `analyze` - Evaluate prompt quality and suggest improvements

**Focus Areas:**
- `intent` - Clarify user's primary objective
- `context` - Gather missing contextual information
- `scope` - Define boundaries and requirements
- `output` - Specify desired response format
- `persona` - Select optimal AI assistant role

## Core Improvement Framework

### 1. Clarification Process
- **Trigger**: Detect ambiguous or vague prompts
- **Method**: Ask up to 3 specific yes/no questions
- **Requirement**: STOP and wait for user response before proceeding
- **Outcome**: Clear understanding of user intent

### 2. Prompt Rewriting
- **Clarity**: Remove ambiguity and add specificity
- **Structure**: Organize requirements logically
- **Context**: Include relevant background information
- **Constraints**: Specify limitations and requirements

### 3. Persona Selection
- **Analysis**: Match task requirements to optimal AI role
- **Justification**: Explain persona choice rationale
- **Specialization**: Leverage domain-specific expertise
- **Communication**: Adjust tone and approach accordingly

### 4. Response Structure
- **8-Section Format**: Apply mandatory structured response framework
- **Consistency**: Ensure all sections properly addressed
- **Quality**: Maintain high standards throughout response
- **Completeness**: Comprehensive coverage of user needs

## Improvement Patterns

### Common Issues and Solutions

**Vague Requests:**
- *Before*: "Help me with my code"
- *After*: "Review the authentication module in src/auth.js for security vulnerabilities and suggest improvements following OWASP guidelines"

**Missing Context:**
- *Before*: "Fix this bug"
- *After*: "Debug the React component rendering issue in UserProfile.jsx where the user avatar displays incorrectly on mobile screens"

**Unclear Output Expectations:**
- *Before*: "Explain this concept"
- *After*: "Provide a comprehensive explanation of microservices architecture with practical examples, benefits, challenges, and implementation recommendations for a team of 5 developers"

**Wrong Persona Match:**
- *Before*: Generic assistant for technical task
- *After*: TDD Coach Agent for test-driven development guidance

## Clarification Question Templates

### Intent Clarification
- "Are you looking for [specific outcome A] or [specific outcome B]?"
- "Should the solution focus on [aspect X] or [aspect Y]?"
- "Do you need [immediate action] or [strategic planning]?"

### Context Gathering
- "Is this for [environment A] or [environment B]?"
- "Are you working with [technology X] or [technology Y]?"
- "Should this integrate with [existing system] or be standalone?"

### Scope Definition
- "Should this cover [narrow scope] or [broader scope]?"
- "Do you need [quick solution] or [comprehensive analysis]?"
- "Is this [one-time task] or [repeatable process]?"

## Implementation Behavior

### Automatic Triggers
1. **Ambiguity Detection**: Identify unclear or vague prompts
2. **Context Analysis**: Assess missing information requirements
3. **Complexity Evaluation**: Determine if clarification needed
4. **Persona Matching**: Select appropriate AI assistant role

### Response Enhancement
1. **Structured Formatting**: Apply 8-section response framework
2. **Quality Assurance**: Ensure comprehensive coverage
3. **Clarity Optimization**: Remove ambiguity and add precision
4. **Value Maximization**: Focus on most helpful response format

### Iterative Refinement
1. **Initial Assessment**: Evaluate prompt quality
2. **Targeted Questions**: Ask specific clarifying questions
3. **Enhanced Rewrite**: Create improved prompt version
4. **Validation**: Confirm understanding before proceeding

## Output Examples

### Clarification Output
```
I need to clarify a few things to provide the best assistance:

1. Are you looking for code review feedback or implementation guidance?
2. Should this focus on security vulnerabilities or performance optimization?
3. Do you need immediate fixes or a comprehensive refactoring plan?

Please answer these questions so I can provide targeted help.
```

### Improved Prompt Output
```
**Original Prompt**: "Help me with my code"

**Improved Prompt**: "Conduct a comprehensive code review of the user authentication system in /src/auth/, focusing on security vulnerabilities, OWASP compliance, and performance optimization. Provide specific recommendations for improvements with implementation priorities."

**Selected Persona**: Code Quality Guardian Agent
**Rationale**: Security focus and comprehensive review requirements match quality assurance expertise.
```

## Success Criteria

- Ambiguous prompts successfully clarified
- User intent accurately understood
- Optimal AI persona selected
- Enhanced prompts enable better assistance
- Structured response framework properly applied
- User satisfaction with improved clarity

## Quality Standards

### Clarification Quality
- **Specific Questions**: Focused, answerable queries
- **Limited Scope**: Maximum 3 questions per iteration
- **Clear Options**: Yes/no or multiple choice format
- **Progressive Refinement**: Build understanding incrementally

### Improvement Quality
- **Clarity Enhancement**: Remove all ambiguity
- **Context Addition**: Include relevant background
- **Specificity**: Precise requirements and constraints
- **Actionability**: Enable immediate productive response

## Integration

Works seamlessly with:
- All AI personas for optimal role selection
- 8-section response structure for consistent output
- Memory bank system for context enhancement
- Quality standards for improvement validation
- User workflow optimization for better assistance