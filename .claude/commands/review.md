# Code Quality Review Command

Comprehensive code quality analysis with SOLID principles enforcement, code smell detection, and actionable improvement recommendations.

## Command

`/review`

## Purpose

Conduct thorough code quality analysis focusing on SOLID principles, anti-pattern detection, code smell identification, and provide specific, prioritized improvement recommendations.

## Usage

```
/review [scope] [focus]
```

**Scope:**
- `file` - Review specific file
- `module` - Review entire module/package
- `project` - Complete project review
- `recent` - Review recent changes
- `pr` - Pull request review simulation

**Focus Areas:**
- `solid` - SOLID principles compliance
- `smells` - Code smell detection
- `patterns` - Anti-pattern identification
- `security` - Security vulnerability analysis
- `performance` - Performance optimization review
- `maintainability` - Long-term maintenance assessment

## Review Framework

### SOLID Principles Analysis

#### Single Responsibility Principle (SRP)
**Assessment:**
- Each class/module has one reason to change
- Functionality is properly focused and cohesive
- Mixed responsibilities are identified and separated

**Violations to Detect:**
- Classes handling multiple unrelated concerns
- Methods performing multiple distinct operations
- Modules with excessive or diverse responsibilities

#### Open/Closed Principle
**Assessment:**
- Code is open for extension, closed for modification
- Proper abstraction and interface usage
- Plugin/strategy pattern implementation

**Violations to Detect:**
- Frequent modification of existing code for new features
- Switch statements that require updates for new cases
- Lack of abstraction for varying behavior

#### Liskov Substitution Principle
**Assessment:**
- Subtypes are substitutable for base types
- Inheritance hierarchies are properly designed
- Polymorphism is correctly implemented

**Violations to Detect:**
- Subclasses that change expected behavior
- Empty or exception-throwing method overrides
- Type checking instead of polymorphism

#### Interface Segregation Principle
**Assessment:**
- Interfaces are focused and cohesive
- Clients depend only on methods they use
- No forced dependency on unused functionality

**Violations to Detect:**
- Large, monolithic interfaces
- Clients implementing empty methods
- Interface pollution with unrelated methods

#### Dependency Inversion Principle
**Assessment:**
- High-level modules independent of low-level modules
- Both depend on abstractions
- Dependency injection proper usage

**Violations to Detect:**
- Direct instantiation of concrete classes
- High-level business logic depending on implementation details
- Lack of abstraction layers

### Code Smell Detection

#### Structural Issues
**Large Components:**
- Methods exceeding 20 lines (max 30 for complex cases)
- Classes with excessive responsibilities ("God Objects")
- Long parameter lists (>3-4 parameters)

**Feature Envy:**
- Methods primarily interested in other classes' data
- Inappropriate delegation of responsibilities
- Poor encapsulation boundaries

#### Design Issues
**Divergent Change / Shotgun Surgery:**
- Single changes requiring multiple class modifications
- Related functionality scattered across multiple classes
- Poor module cohesion

**Data Clumps:**
- Related variables frequently passed together
- Missing encapsulation opportunities
- Primitive obsession patterns

**Message Chains:**
- Deep method call chains (a.getB().getC().doSomething())
- Law of Demeter violations
- Excessive coupling between objects

#### Behavioral Issues
**Inappropriate Intimacy:**
- Classes knowing too much about each other's internals
- Excessive coupling and dependency
- Breaking encapsulation boundaries

**Refused Bequest:**
- Subclasses not using parent methods/properties
- Incorrect inheritance hierarchies
- Composition over inheritance opportunities

### Anti-Pattern Detection

#### Implementation Anti-Patterns
**Hard-Coded Values:**
- Magic numbers and strings in code
- Missing configuration management
- Lack of constants and enums

**Premature Optimization:**
- Complex optimizations without performance measurement
- Sacrificing readability for unproven performance gains
- Over-engineering solutions

**Reinventing the Wheel:**
- Custom implementations of standard functionality
- Not leveraging existing libraries and frameworks
- Duplicate code across modules

#### Error Handling Anti-Patterns
**Error Hiding:**
- Silent exception catching
- Inadequate error logging
- Missing error propagation

**Exceptions for Flow Control:**
- Using exceptions for normal program logic
- Performance impact of exception-based control
- Poor separation of exceptional vs. normal cases

#### Architecture Anti-Patterns
**Circular Dependencies:**
- Modules depending on each other circularly
- Difficult testing and maintenance
- Architectural coupling issues

**Anemic Domain Model:**
- Business logic in service layers instead of domain objects
- Data structures without behavior
- Poor object-oriented design

## Review Process

### 1. Initial Analysis
**Context Understanding:**
- Read and understand code purpose and functionality
- Identify primary quality concerns and areas of focus
- Map code structure and component relationships

**Quality Baseline:**
- Assess current quality level
- Identify most critical issues
- Prioritize review focus areas

### 2. Systematic Review
**SOLID Compliance:**
- Evaluate each principle systematically
- Document specific violations with examples
- Provide concrete improvement recommendations

**Code Smell Identification:**
- Scan for structural, design, and behavioral issues
- Categorize and prioritize identified problems
- Suggest specific refactoring strategies

**Anti-Pattern Detection:**
- Identify implementation, error handling, and architecture anti-patterns
- Assess impact and urgency of each issue
- Recommend remediation approaches

### 3. Quality Assessment
**Maintainability Evaluation:**
- Code readability and structure assessment
- Documentation adequacy review
- Long-term maintenance considerations

**Security Analysis:**
- Security vulnerability identification
- Best practices compliance verification
- Risk assessment and mitigation recommendations

**Performance Review:**
- Algorithmic efficiency analysis
- Resource usage optimization opportunities
- Scalability considerations

### 4. Recommendations
**Prioritized Improvements:**
- High-impact, low-effort quick wins
- Critical issues requiring immediate attention
- Long-term architectural improvements

**Implementation Guidance:**
- Step-by-step refactoring instructions
- Risk assessment for proposed changes
- Testing strategy for improvements

## Review Output Format

### Executive Summary
```markdown
## Code Quality Review Summary

**Overall Quality Score**: [A-F rating]
**Critical Issues**: [Number] 
**Major Issues**: [Number]
**Minor Issues**: [Number]

**Primary Recommendations**:
1. [Highest priority improvement]
2. [Second priority improvement]
3. [Third priority improvement]
```

### Detailed Analysis
```markdown
## SOLID Principles Compliance

### Single Responsibility Principle: [PASS/FAIL]
**Issues Found**:
- [File:Line] - [Specific violation description]
- [File:Line] - [Specific violation description]

**Recommendations**:
- [Specific refactoring suggestion]
- [Implementation guidance]

## Code Smells Detected

### Large Components
**Issues**:
- [File:Line] - [Method too long: X lines]
- [File:Line] - [Class too complex: Y responsibilities]

**Refactoring Strategy**:
- [Extract method/class recommendations]
- [Specific improvement steps]

## Anti-Patterns Identified

### Hard-Coded Values
**Locations**:
- [File:Line] - [Magic number/string]

**Solutions**:
- [Constants/configuration recommendations]
```

## Command Examples

### Scope-Specific Reviews
```bash
/review file UserService.java        # Review specific file
/review module authentication        # Review auth module
/review project                      # Complete project review
/review recent                       # Review recent changes
```

### Focus-Specific Reviews
```bash
/review solid payment-processing     # SOLID compliance check
/review smells user-interface        # Code smell detection
/review security api-endpoints       # Security vulnerability review
/review performance data-processing  # Performance optimization review
```

### Comprehensive Reviews
```bash
/review pr feature-branch            # Complete PR review
/review maintainability legacy-code  # Long-term maintenance assessment
```

## Success Criteria

- Complete SOLID principles compliance assessment
- Comprehensive code smell identification
- Anti-pattern detection and remediation guidance
- Prioritized improvement recommendations
- Actionable refactoring instructions
- Quality score and progress tracking

## Quality Metrics

### Code Quality Indicators
- **Maintainability**: Readability, structure, documentation
- **Modularity**: Separation of concerns, coupling, cohesion
- **Testability**: Test coverage, mock-ability, isolation
- **Extensibility**: Flexibility, abstraction, plugin capability
- **Performance**: Efficiency, scalability, resource usage

### Review Effectiveness
- Issue identification accuracy
- Recommendation relevance and actionability
- Implementation success rate
- Long-term quality improvement
- Developer learning and skill enhancement

## Integration

Works seamlessly with:
- Code Quality Guardian Agent for expert analysis
- TDD Coach Agent for testing-focused reviews
- Planning Specialist Agent for architectural review
- Security best practices for vulnerability assessment
- Performance optimization guidelines
- Memory bank system for quality tracking and history