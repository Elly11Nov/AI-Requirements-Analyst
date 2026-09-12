# Requirements Engineering Approach

## Overview

Requirements engineering provides the framework for moving from an initial problem or idea to a solution that can be defined, developed and validated.

My approach combines requirements analysis, information architecture, process modelling and iterative validation.

I use AI as an assistant where it can accelerate analysis or identify areas that need attention, while keeping human judgement and validation at the centre of the process.

The approach is demonstrated through two case studies:

- **LinkedIn Insights** — analysing a professional network to support job searching and networking.
- **Deal Compass** — analysing investment terms to support startup decision-making.

The aim is to understand the problem before defining the solution and to maintain a clear connection between user needs, requirements and the resulting product.

## The Requirements Engineering Process

The overall approach can be represented as:

    Problem or opportunity
            ↓
    Stakeholders and users
            ↓
    Goals and needs
            ↓
    Requirements
            ↓
    Analysis and modelling
            ↓
    Prioritisation
            ↓
    Solution definition
            ↓
    Acceptance criteria
            ↓
    Validation
            ↓
    Iteration

The process is not necessarily linear.

New information, stakeholder feedback or validation findings may require earlier requirements to be revisited.

## 1. Understand the Problem

The first step is to understand the problem that needs to be solved.

I avoid starting with a predefined technical solution wherever possible.

Instead, I ask:

- What problem are we trying to solve?
- Who experiences the problem?
- What are they trying to achieve?
- What happens today?
- What would a successful outcome look like?

For example, the starting point for LinkedIn Insights is not "build a dashboard".

The underlying problem is that a professional network can contain useful information that is difficult to identify and use efficiently during a job search.

For Deal Compass, the starting point is not simply "build a calculator".

The underlying problem is that investment terms can contain several financial and governance implications that need to be understood together.

## 2. Identify Stakeholders and Users

Requirements need to be considered from the perspective of the people affected by the solution.

I identify:

- Primary users
- Secondary users
- Business stakeholders
- Technical stakeholders
- Operational or support stakeholders

The level of stakeholder analysis depends on the project.

For the two portfolio case studies, the primary users are:

| Case study | Primary user | Main objective |
|---|---|---|
| LinkedIn Insights | Job seeker | Identify and use relevant professional connections |
| Deal Compass | Startup founder | Understand and compare investment terms |

Identifying the user and their objective provides context for the requirements that follow.

## 3. Define Goals and Outcomes

Goals describe what the user or organisation wants to achieve.

They should be expressed in terms of outcomes rather than interface features.

For example:

### LinkedIn Insights

**Goal:** Identify professional connections that may be useful during a job search.

### Deal Compass

**Goal:** Understand and compare the implications of a proposed investment.

These goals provide a reference point when deciding whether a proposed requirement is actually useful.

## 4. Elicit Requirements

Requirements can come from many sources, including:

- User needs
- Business objectives
- Existing processes
- Existing systems
- Documentation
- Data
- Stakeholder knowledge
- Regulatory or organisational constraints
- Problems identified during analysis

The source of a requirement matters.

A requirement based on an explicit business need should be distinguished from an assumption or suggestion made during solution design.

Where information is incomplete, I identify the gap rather than filling it with an unsupported assumption.

## 5. Analyse and Structure Requirements

Once requirements have been identified, they need to be organised.

I consider:

- Functional requirements
- Non-functional requirements
- Business rules
- Data requirements
- User interactions
- Dependencies
- Constraints
- Assumptions
- Exceptions

For example:

    User need
        ↓
    Functional requirement
        ↓
    Business rule
        ↓
    System behaviour
        ↓
    Expected outcome

Structuring requirements in this way helps reveal relationships and dependencies that may not be obvious in an unstructured list.

## 6. Separate Requirements from Solutions

A requirement describes **what is needed**.

A solution describes **how the need will be addressed**.

For example:

> The user needs to identify relevant professional connections.

is a requirement.

> Provide a dashboard with a company filter.

is a possible solution.

Keeping these separate during analysis helps avoid committing to a particular implementation before the underlying need is understood.

The final solution may change while the underlying requirement remains valid.

## 7. Identify Business Rules

Some requirements depend on rules that determine how the solution behaves.

Business rules may define:

- Calculations
- Conditions
- Eligibility
- Dependencies
- Valid values
- Processing logic
- Relationships between data elements

Deal Compass provides an example where financial calculations and investment terms influence the results presented to the user.

The analysis therefore needs to distinguish between:

    User input
        ↓
    Business rules
        ↓
    Calculated result
        ↓
    Decision-support information

Making these relationships explicit helps prevent business logic from becoming hidden inside interface requirements.

## 8. Model Information and Processes

Text alone is not always the best way to communicate a requirement.

I use models and diagrams where they make relationships, processes or system behaviour easier to understand.

Depending on the problem, these may include:

- Use case diagrams
- Activity diagrams
- Process workflows
- Sequence diagrams
- Data or domain models

For example, a simplified LinkedIn Insights workflow might be:

    Import connections
          ↓
    Process information
          ↓
    Search or filter
          ↓
    Identify relevant connections
          ↓
    Review results

A simplified Deal Compass workflow might be:

    Enter investment terms
          ↓
    Calculate results
          ↓
    Model scenarios
          ↓
    Compare outcomes
          ↓
    Review decision-support information

The purpose of modelling is to make the requirement easier to understand and validate.

## 9. Manage Assumptions, Constraints and Unknowns

Requirements are often developed before all information is available.

I therefore distinguish between:

| Category | Meaning |
|---|---|
| Known | Supported by available information |
| Assumption | Used temporarily but not yet confirmed |
| Constraint | Limits the possible solution |
| Unknown | Information that still needs to be established |

This distinction is important because assumptions can otherwise become embedded in requirements and later be mistaken for confirmed facts.

For example, the LinkedIn Insights prototype works with an imported connection dataset rather than a direct LinkedIn integration.

That is a known characteristic of the prototype.

Whether a production system would require a different integration approach is a separate question.

## 10. Identify Gaps and Ambiguity

Good requirements analysis should reveal what is not yet understood.

Examples include:

- Vague terminology
- Missing business rules
- Unclear user expectations
- Missing data
- Conflicting requirements
- Undefined exceptions
- Unclear ownership
- Requirements that cannot currently be tested

For example:

> "The system should identify relevant contacts."

requires further clarification.

What makes a contact relevant?

What information determines relevance?

Who defines the criteria?

What should happen when no relevant contacts are found?

Rather than silently interpreting the requirement, I would record the ambiguity and seek clarification.

## 11. Prioritise Requirements

Requirements need to be prioritised because not everything can or should be delivered at once.

A simple approach is:

| Priority | Meaning |
|---|---|
| Must have | Essential to the core purpose |
| Should have | Important but not essential to the initial solution |
| Could have | Useful enhancement |
| Won't have | Outside the current scope |

Prioritisation helps establish a realistic scope and keeps the core user need visible.

It also provides a basis for making trade-offs when time, resources or technical constraints change.

## 12. Translate Requirements into User Stories

Where an Agile approach is appropriate, requirements can be expressed as user stories.

A common format is:

> As a [user], I want to [action], so that [benefit].

For example:

> As a job seeker, I want to filter my connections by company so that I can identify people who may be relevant to a job opportunity.

Or:

> As a founder, I want to compare investment scenarios so that I can understand how different terms affect the proposed deal.

The user story captures the user need without prescribing the technical implementation.

## 13. Define Acceptance Criteria

Acceptance criteria make requirements testable.

For example:

**Requirement**

The user can filter connections by company.

**Acceptance criteria**

- The user can enter or select a company.
- The system identifies matching connections.
- The matching results are displayed to the user.
- The system indicates when no matching connections are found.

Acceptance criteria provide a shared understanding of what "done" means.

They can also support testing and validation later in the development process.

## 14. Validate Requirements

Requirements should be reviewed before they become the basis for implementation.

I consider questions such as:

### Is it clear?

Could different people interpret it differently?

### Is it necessary?

Does it support an identified need?

### Is it feasible?

Can it be implemented within the known constraints?

### Is it testable?

Can we determine whether it has been satisfied?

### Is it consistent?

Does it conflict with another requirement?

### Is it traceable?

Can it be connected to the original user or business need?

Validation may result in requirements being clarified, changed, split, combined or removed.

## 15. Use AI Where It Adds Value

AI can support requirements engineering, particularly when information is unstructured or large in volume.

I see useful applications in areas such as:

- Extracting potential requirements
- Structuring unstructured information
- Identifying ambiguity
- Suggesting clarification questions
- Grouping related requirements
- Identifying potential conflicts
- Generating initial user stories
- Suggesting acceptance criteria
- Reviewing terminology
- Supporting process analysis
- Identifying possible gaps

However, AI output is treated as a starting point for analysis rather than as an authoritative requirement.

A controlled workflow is:

    Source information
          ↓
    AI-assisted analysis
          ↓
    Potential requirements
          ↓
    Human review
          ↓
    Validated requirements
          ↓
    Solution definition

The analyst remains responsible for deciding whether a proposed requirement is relevant, accurate and supported by the available information.

## 16. Maintain Traceability

Traceability provides a connection between the original need and the resulting solution.

A simple chain is:

    Business need
          ↓
    Requirement
          ↓
    User story
          ↓
    Acceptance criteria
          ↓
    Solution
          ↓
    Validation

Traceability helps answer questions such as:

- Why does this feature exist?
- Which requirement does it satisfy?
- How will it be tested?
- What could be affected if the requirement changes?

It also helps prevent features from being added without a clear connection to a user or business need.

## 17. Iterate

Requirements rarely remain completely static.

New information may emerge through:

- Stakeholder feedback
- Prototyping
- Testing
- Technical investigation
- Changes in business priorities
- New constraints
- User feedback

The requirements process should therefore support iteration.

A prototype can be particularly useful because it gives stakeholders something concrete to react to.

This creates a feedback loop:

    Requirements
         ↓
    Prototype
         ↓
    Review
         ↓
    New information
         ↓
    Refined requirements
         ↓
    Improved solution

The objective is not to predict everything perfectly at the beginning, but to create a controlled way of learning and refining the solution.

## Requirements Engineering Checklist

    [ ] Problem and desired outcome understood
    [ ] Users and stakeholders identified
    [ ] Goals defined
    [ ] Requirements elicited
    [ ] Functional requirements identified
    [ ] Non-functional requirements considered
    [ ] Business rules identified
    [ ] Data requirements considered
    [ ] Assumptions recorded
    [ ] Constraints identified
    [ ] Gaps and ambiguities identified
    [ ] Requirements prioritised
    [ ] Use cases defined where appropriate
    [ ] User stories defined where appropriate
    [ ] Acceptance criteria defined
    [ ] Processes and relationships modelled where useful
    [ ] Requirements reviewed for clarity and consistency
    [ ] Requirements validated
    [ ] Traceability considered
    [ ] AI-generated suggestions reviewed by a human
    [ ] Requirements revisited as new information becomes available

## Case Studies

The approach described here is applied to two existing prototypes.

### LinkedIn Insights

The analysis focuses on:

- User needs during job searching
- Professional connection data
- Information organisation
- Search and filtering
- Identifying relevant contacts
- User workflows
- Potential requirements and acceptance criteria

See the [LinkedIn Insights case study](../case%20studies/linkedin-insights.md).

### Deal Compass

The analysis focuses on:

- Founder needs
- Investment information
- Financial calculations
- Business rules
- Scenario modelling
- Decision-support requirements
- User workflows
- Acceptance criteria

See the [Deal Compass case study](../case%20studies/deal-compass.md).

## Key Principle

Requirements engineering is not about predicting every detail of a solution before development begins.

It is about creating a clear, traceable and testable connection between the problem, the people who need the solution and what the solution must achieve.

> **Understand the problem, make the requirements explicit, validate the assumptions, and let the solution evolve from evidence.**
