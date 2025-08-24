# Business Analysis Workflow Command

Structured business analyst collaboration for epic decomposition, user story generation, and acceptance criteria development.

## Command

`/ba`

## Purpose

Guide Business Analysts through systematic user story creation, epic decomposition, and requirements analysis using proven agile methodologies and collaborative design principles.

## Usage

```
/ba [stage] [focus]
```

**Stages:**
- `start` - Initialize BA collaboration session
- `scope` - Stage 1: Scope Understanding
- `epic` - Stage 2: Epic Decomposition
- `stories` - Stage 3: Story Detailing & Acceptance Criteria
- `review` - Stage 4: Review & Planning
- `validate` - Validate complete deliverable

**Focus Areas:**
- `feature` - Feature epic development
- `enhancement` - Enhancement story creation
- `user-journey` - User experience mapping
- `acceptance` - Acceptance criteria refinement
- `personas` - User persona development

## BA Collaboration Framework

### Core Interaction Model
**Disciplined "Pause-Ask-Refine-Continue" Protocol:**

1. **Clarification**: Follow structured response guidelines for prompt clarification
2. **Focused Updates**: Update only one document section at a time
3. **Explicit Confirmation**: Request BA review and consent after each update
4. **Disagreement Handling**: Up to 3 refinement cycles per section if BA disagrees
5. **Scope Management**: Warn of quality risks if steps are skipped
6. **Professional Deliverables**: Format for direct integration into BA tools

### User Story Development Principles

1. **Communication Catalysts**: Stories spark conversation, not just specifications
2. **Strategic Context**: Use story maps to visualize user journeys and dependencies
3. **Vertical Slicing**: Deliver end-to-end value across all technical layers
4. **Collaborative Design**: Use Acceptance Criteria for collaborative design before development
5. **Narrative Information**: Convert raw data into user-centered narratives
6. **Methodical Decomposition**: Break epics into independent, valuable, sprint-sized stories
7. **INVEST Criteria**: Ensure stories are Independent, Negotiable, Valuable, Estimable, Small, Testable
8. **Value & Resilience**: Embed business value and system resilience focus

## BA Workflow Stages

### Stage 1: Scope Understanding
**Objective**: Clarify initial epic/feature concept and establish foundation

**Process:**
1. Clarify initial epic/feature concept and business context
2. Understand business objectives, constraints, and success criteria
3. Identify key stakeholders and primary user types
4. Establish acceptance thresholds and value measurements

**Activities:**
- Epic concept clarification and refinement
- Business objective identification and validation
- Stakeholder mapping and role definition
- Success criteria establishment

**Deliverables:**
- Clear epic description and business rationale
- Stakeholder identification and roles
- Success criteria and value metrics
- Scope boundaries and constraints

### Stage 2: Epic Decomposition
**Objective**: Break down epic into manageable, valuable user stories

**Process:**
1. Analyze epic scope and identify major functionality areas
2. Apply vertical slicing principles to create end-to-end value stories
3. Ensure INVEST criteria compliance for each story
4. Map story dependencies and relationships
5. Request user review and confirmation

**Epic Decomposition Principles:**
- **Vertical Slicing**: Stories deliver complete user value
- **Independent Value**: Each story provides standalone business benefit
- **Appropriate Sizing**: Stories fit within sprint capacity
- **Dependency Mapping**: Clear understanding of story relationships
- **Priority Alignment**: Business value-driven story ordering

**Output Structure:**
```markdown
## Epic Description / Feature Overview
[High-level business objective and value proposition]

## User Personas (when applicable)
[Target user types and characteristics]

## User Story Map Snippets
[Visual representation with Mermaid diagrams where valuable]

## User Stories Overview
1. [Story Title] - [Brief description]
2. [Story Title] - [Brief description]
[Continue for all identified stories]
```

### Stage 3: Story Detailing & Acceptance Criteria
**Objective**: Refine story narratives and define comprehensive acceptance criteria

**Process:**
1. Develop detailed user story narratives using standard format
2. Define comprehensive acceptance criteria in Given-When-Then format
3. Ensure testable and measurable outcomes for each criterion
4. Validate business value proposition and user benefit
5. Request user review and confirmation

**User Story Template:**
```markdown
### Story [X]: [Title]

#### Narrative
As a [user persona],
I want [specific functionality],
So that [business value/benefit].

#### Acceptance Criteria
**Scenario 1: [Primary flow]**
- Given [initial condition]
- When [user action]
- Then [expected outcome]

**Scenario 2: [Alternative flow]**
- Given [alternative condition]
- When [different action]
- Then [alternative outcome]

**Scenario 3: [Error handling]**
- Given [error condition]
- When [action triggers error]
- Then [error handling outcome]

#### Definition of Done
- [ ] [Technical implementation criteria]
- [ ] [Testing requirements]
- [ ] [Documentation updates]
- [ ] [Acceptance testing completion]
```

**Acceptance Criteria Quality Standards:**
- **Specific and Measurable**: Clear, verifiable outcomes
- **Given-When-Then Format**: Consistent scenario structure
- **Comprehensive Coverage**: All important scenarios included
- **Business Rule Documentation**: Rules and constraints captured
- **Edge Case Consideration**: Boundary and error conditions addressed

### Stage 4: Review & Planning
**Objective**: Analyze for gaps, dependencies, and define implementation approach

**Process:**
1. Review complete story suite for gaps and inconsistencies
2. Analyze story dependencies and implementation sequencing
3. Identify risks, assumptions, and open questions
4. Define next steps and implementation priorities
5. Request final user review and approval

**Review Components:**
- **Gap Analysis**: Missing functionality identification
- **Dependency Mapping**: Story relationships and sequencing
- **Risk Assessment**: Implementation challenges and mitigation
- **Stakeholder Validation**: Business alignment confirmation

**Output Structure:**
```markdown
## Open Questions / Points for Clarification
1. [Question requiring stakeholder input]
2. [Technical clarification needed]
3. [Business rule validation required]

## Dependencies and Risks
### Story Dependencies
- [Story A] must be completed before [Story B]

### Implementation Risks
- [Risk description] - [Mitigation strategy]

## Next Steps
1. [Immediate action item]
2. [Stakeholder communication needed]
3. [Technical analysis required]
```

## Document Management

### Standard Document Architecture
Creates structured Markdown file (e.g., `feature-x-user-stories.md`):

```markdown
# [Epic/Feature Name] User Stories

## Epic Description / Feature Overview
[Business context and objectives]

## User Personas (when applicable)
[Target user types and characteristics]

## User Story Map Snippets (with Mermaid diagrams where valuable)
[Visual user journey representation]

## User Stories

### Story 1: [Title]
#### Narrative
[As a... I want... So that... format]

#### Acceptance Criteria
[Given-When-Then scenarios]

[Continue for all stories...]

## Open Questions / Points for Clarification
[Unresolved issues requiring input]

## Next Steps
[Implementation planning and actions]
```

## Command Examples

### BA Session Management
```bash
/ba start user-authentication      # Begin BA session for auth feature
/ba validate payment-integration   # Validate complete payment stories
```

### Stage-Specific Work
```bash
/ba scope mobile-checkout          # Clarify mobile checkout epic
/ba epic e-commerce-platform       # Decompose e-commerce epic
/ba stories user-profile           # Detail user profile stories
/ba review notification-system     # Review notification stories
```

### Specialized BA Work
```bash
/ba personas customer-portal       # Develop customer portal personas
/ba acceptance order-management    # Refine order management criteria
/ba user-journey shopping-cart     # Map shopping cart user journey
```

## Quality Standards

### Epic Quality Criteria
- **Clear Business Value**: Articulated business benefit and rationale
- **Appropriate Scope**: Manageable size for development iteration
- **Stakeholder Alignment**: Business and technical stakeholder agreement
- **Success Metrics**: Measurable outcomes and acceptance criteria

### User Story Quality Criteria
- **INVEST Compliance**: Independent, Negotiable, Valuable, Estimable, Small, Testable
- **Clear Narrative**: User-focused language and benefit articulation
- **Comprehensive Acceptance Criteria**: Complete scenario coverage
- **Testable Outcomes**: Verifiable and measurable results

### Documentation Quality
- **Professional Formatting**: Clear structure and presentation
- **Stakeholder Communication**: Appropriate language and detail level
- **Tool Integration**: Compatible with BA and development tools
- **Version Control**: Change tracking and collaboration support

## Success Criteria

- High-quality epic decomposition into valuable stories
- Comprehensive acceptance criteria enabling development
- INVEST criteria compliance across all stories
- Stakeholder alignment and business value clarity
- Professional deliverables ready for development handoff
- Enhanced BA workflow efficiency and effectiveness

## Integration

Works seamlessly with:
- Business Analyst Agent for expert guidance
- Planning Specialist Agent for implementation planning
- TDD Coach Agent for acceptance criteria testing
- Test Architect Agent for acceptance testing strategy
- Code Quality Guardian Agent for implementation quality
- Memory bank system for requirements persistence