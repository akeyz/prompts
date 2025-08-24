# Test-Driven Development Command

Initialize and guide TDD workflow through structured 4-phase development cycle with expert coaching and best practices enforcement.

## Command

`/tdd`

## Purpose

Launch comprehensive Test-Driven Development sessions with systematic phase guidance, quality enforcement, and educational support for effective TDD implementation.

## Usage

```
/tdd [phase] [target]
```

**Phases:**
- `start` - Initialize new TDD session
- `prepare` - Phase 0: Preparation & Understanding
- `design` - Phase 1: Conceptual Design (no code)
- `test` - Phase 2: Test Implementation
- `implement` - Phase 3: Code Implementation
- `review` - Phase 4: Review & Finalize
- `cycle` - Complete Red-Green-Refactor cycle

**Targets:**
- `feature` - TDD for new feature development
- `bug` - TDD approach for bug fixing
- `refactor` - TDD-guided refactoring
- `component` - Component-specific TDD
- `integration` - Integration testing with TDD

## TDD Workflow Phases

### Phase 0: Preparation & Understanding
**Objective**: Establish clear foundation for TDD session

**Activities:**
1. Read project memory bank for complete context
2. Clarify technical requirements and acceptance criteria
3. Decompose complex tasks using MECE principles
4. Establish clear objectives and success criteria

**Deliverables:**
- Clear understanding of requirements
- Task decomposition plan
- Success criteria definition
- TDD session objectives

### Phase 1: Design (Conceptual) - NO CODE
**Objective**: Create comprehensive design without implementation

**Activities:**
1. Define system/module architecture
2. Design classes, methods, and relationships
3. Plan component interactions and dependencies
4. Create conceptual test case designs

**Constraints:**
- **Absolutely no implementation or test code**
- Focus on design and architecture only
- Use diagrams and structured documentation

**Deliverables:**
- System architecture design
- Component relationship diagrams
- Conceptual test case plans
- Design validation checklist

### Phase 2: Test Implementation (TDD)
**Objective**: Implement failing tests based on design

**Activities:**
1. Write failing tests for each designed component
2. Ensure tests fail for the right reasons
3. Follow Red-Green-Refactor cycle principles
4. Maintain test independence and clarity

**Best Practices:**
- Clear, descriptive test names
- Independent test execution
- Meaningful failure messages
- Comprehensive scenario coverage

**Deliverables:**
- Complete failing test suite
- Test execution validation
- Coverage gap analysis
- Red phase confirmation

### Phase 3: Code Implementation
**Objective**: Write minimal code to make tests pass

**Activities:**
1. Implement minimal production code for test passage
2. Adhere strictly to Phase 1 design specifications
3. Refactor for quality while maintaining green tests
4. Apply SOLID principles and quality standards

**Guidelines:**
- Write only enough code to pass tests
- Maintain design integrity
- Continuous refactoring for quality
- Regular test execution validation

**Deliverables:**
- Working production code
- All tests passing (Green phase)
- Quality-compliant implementation
- Refactored, clean codebase

### Phase 4: Review & Finalize
**Objective**: Comprehensive validation and documentation

**Activities:**
1. Complete code and test quality review
2. Verify all requirements satisfaction
3. Update project documentation and memory bank
4. Plan next development iterations

**Quality Checks:**
- SOLID principles adherence
- Code smell elimination
- Test coverage validation
- Documentation completeness

**Deliverables:**
- Quality-reviewed codebase
- Updated documentation
- Memory bank updates
- Next steps planning

## Red-Green-Refactor Cycle

### Red Phase
1. Write a failing test for new functionality
2. Verify test fails for expected reasons
3. Confirm test is well-structured and clear
4. Document expected behavior

### Green Phase
1. Write minimal code to make test pass
2. Focus on functionality over optimization
3. Verify all tests pass
4. Maintain existing functionality

### Refactor Phase
1. Improve code structure and quality
2. Eliminate code smells and duplication
3. Apply design patterns appropriately
4. Ensure all tests remain green

## Command Examples

### Session Management
```bash
/tdd start feature          # Begin TDD for new feature
/tdd prepare authentication # Prepare TDD for auth module
/tdd cycle login           # Complete TDD cycle for login
```

### Phase-Specific Commands
```bash
/tdd design user-service   # Design phase for user service
/tdd test validation       # Test implementation for validation
/tdd implement api         # Code implementation for API
/tdd review security       # Review phase for security features
```

### Specialized TDD
```bash
/tdd refactor legacy       # TDD-guided legacy refactoring
/tdd bug payment-issue     # TDD approach to bug fixing
/tdd integration database  # Integration testing with TDD
```

## Quality Standards Integration

### SOLID Principles
- Single Responsibility in design and implementation
- Open/Closed principle in architecture
- Liskov Substitution in inheritance
- Interface Segregation in contracts
- Dependency Inversion in dependencies

### Code Quality
- DRY principle enforcement
- Code smell detection and elimination
- Anti-pattern prevention
- Performance consideration
- Security best practices

### Testing Excellence
- Comprehensive coverage (positive, negative, edge cases)
- Clear and maintainable tests
- Proper assertion usage
- Test independence and reliability
- Meaningful failure messages

## Success Criteria

- Systematic TDD workflow completion
- High-quality, tested code delivery
- Design principles adherence
- Comprehensive test coverage achievement
- Knowledge transfer and skill development
- Sustainable development practices establishment

## Educational Components

### TDD Principles Reinforcement
- Explanation of TDD benefits and rationale
- Best practices guidance and coaching
- Common pitfall identification and avoidance
- Skill development through practice

### Quality Awareness
- Code quality importance and impact
- Design pattern application
- Refactoring techniques and timing
- Continuous improvement mindset

## Integration

Works seamlessly with:
- TDD Coach Agent for expert guidance
- Code Quality Guardian Agent for quality assurance
- Test Architect Agent for testing strategy
- Memory bank system for context persistence
- Planning workflows for requirement clarity
- Review processes for quality validation