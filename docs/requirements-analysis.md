# Requirements Analysis

## Purpose

Requirements analysis is the process of understanding a problem, identifying what users and stakeholders need, and translating those needs into clear, structured and testable requirements.

The objective is not simply to produce a list of features.

A good requirements analysis establishes:

- The problem to be solved
- Who is affected by the problem
- What users need to accomplish
- What the proposed solution needs to do
- What constraints apply
- What assumptions have been made
- What information is still missing
- How the resulting solution can be validated

This approach is demonstrated through two case studies based on existing application prototypes:

- **LinkedIn Insights** — an AI-assisted tool that turns a LinkedIn connection export into information that can support job searching and networking.
- **Deal Compass** — an AI-assisted tool that helps founders analyse and compare key terms in a proposed investment.

The prototypes are maintained in their own repositories. The case studies in this repository focus on the requirements analysis and solution-design perspective behind them.

See:

- [LinkedIn Insights case study](../case%20studies/linkedin-insights.md)
- [Deal Compass case study](../case%20studies/deal-compass.md)

## From Problem to Solution

A useful way to view requirements analysis is:

    Business problem
          ↓
    Users and stakeholders
          ↓
    Goals and needs
          ↓
    Requirements
          ↓
    Use cases
          ↓
    Processes and business rules
          ↓
    Solution definition
          ↓
    Acceptance criteria
          ↓
    Validation

The process is iterative. New information may require requirements to be clarified, changed or prioritised.

The two case studies illustrate how the approach can be applied to different types of problems.

## 1. Understand the Problem

The starting point is the problem rather than the solution.

Before defining features, establish:

- What problem exists?
- Who experiences it?
- Why does it matter?
- What happens today?
- What would a successful outcome look like?

For **LinkedIn Insights**, the problem is not simply "build a dashboard".

The underlying need is to make an existing professional network more useful during a job search by helping the user identify relevant connections and information.

For **Deal Compass**, the problem is not simply "build a term sheet calculator".

The underlying need is to help a founder understand the financial and governance implications of proposed investment terms and compare different scenarios.

Starting with the problem helps avoid defining the solution too early.

## 2. Identify Users and Stakeholders

Different people may have different goals and expectations of the same system.

Identify:

- Primary users
- Secondary users
- Business stakeholders
- Technical stakeholders
- People responsible for maintaining or supporting the solution

For these case studies, the primary user is clear:

| Case study | Primary user |
|---|---|
| LinkedIn Insights | Job seeker |
| Deal Compass | Startup founder |

The analysis can then focus on what each user needs to accomplish.

For LinkedIn Insights, the user needs to find and interpret useful information about professional connections.

For Deal Compass, the user needs to understand and compare the implications of investment terms.

## 3. Define Goals

Goals describe the outcome the user wants to achieve.

For example:

### LinkedIn Insights

> Identify professional connections that may be relevant to a job search.

### Deal Compass

> Understand and compare the implications of proposed investment terms.

Goals provide context for the requirements that follow.

They also provide a basis for evaluating whether the proposed solution is solving the right problem.

## 4. Identify Functional Requirements

Functional requirements describe what the solution must do.

For example, LinkedIn Insights needs to support activities such as:

- Importing connection data
- Organising available connection information
- Filtering or searching information
- Identifying relevant contacts
- Displaying results

Deal Compass needs to support activities such as:

- Capturing investment terms
- Performing financial calculations
- Representing ownership and other deal terms
- Modelling different scenarios
- Comparing results

A functional requirement should describe a behaviour or capability rather than simply naming a feature.

For example:

> The system shall allow the user to filter connections by company.

is more useful than:

> Company filter.

## 5. Identify Non-Functional Requirements

Non-functional requirements describe qualities, constraints or characteristics of the solution.

Depending on the system, these may include:

- Performance
- Usability
- Accessibility
- Security
- Reliability
- Maintainability
- Scalability
- Compatibility

Not every project requires the same set of non-functional requirements.

They should be identified according to the context and intended use of the solution.

For example, a tool intended for users who are analysing large amounts of information may place greater emphasis on usability and clarity of presentation.

## 6. Identify Business Rules

Business rules define conditions, calculations or constraints that influence how the solution behaves.

This is particularly relevant to **Deal Compass**, where some results are derived from financial inputs and defined calculation rules.

Requirements analysis needs to distinguish between:

- User input
- Stored information
- Calculated values
- Business rules
- Displayed results

For example:

    User enters investment terms
             ↓
    Business rules and calculations
             ↓
    Calculated results
             ↓
    User compares scenarios

Separating business rules from interface design makes the underlying logic easier to understand, test and maintain.

## 7. Identify Data Requirements

Requirements analysis should consider the information the solution needs to work with.

Questions include:

- What data is required?
- Where does it come from?
- What information does the user provide?
- What information is calculated?
- What relationships exist between data elements?
- What information needs to be displayed?

### LinkedIn Insights

The analysis involves information such as:

    Connection
        ├── Person
        ├── Company
        └── Location

This helps establish how connection information can be organised and analysed.

### Deal Compass

The analysis involves information such as:

    Investment
        ├── Amount
        ├── Valuation
        ├── Ownership
        ├── Terms
        └── Scenarios

The level of modelling should reflect the complexity of the problem rather than creating unnecessary detail.

## 8. Identify Assumptions and Constraints

Requirements are often developed with incomplete information.

It is therefore important to distinguish between:

**Known information**

Information supported by the available evidence.

**Assumptions**

Information being used temporarily because it has not yet been confirmed.

**Constraints**

Conditions that restrict the possible solution.

**Unknowns**

Information that still needs to be established.

For example, in LinkedIn Insights:

| Type | Example |
|---|---|
| Known | Connection data is imported from a CSV export |
| Constraint | The prototype does not require direct access to LinkedIn |
| Unknown | Whether future versions would require external integrations |

For Deal Compass:

| Type | Example |
|---|---|
| Known | The prototype models investment terms and scenarios |
| Constraint | The prototype is intended as decision support rather than legal or investment advice |
| Unknown | Which additional deal structures might be required in a production system |

Making these distinctions explicit reduces the risk of building requirements around assumptions.

## 9. Identify Gaps and Ambiguities

A requirement can appear clear while still leaving important questions unanswered.

For example:

> "The system should identify relevant contacts."

This raises questions:

- Relevant according to which criteria?
- Who defines relevance?
- What information is used?
- Can the user change the criteria?
- What should happen if no matches are found?

Similarly, a requirement such as:

> "The system should compare investment scenarios."

raises questions about:

- Which values are compared?
- Which assumptions are used?
- Which scenarios are supported?
- How are differences presented?

Requirements analysis should expose these questions rather than silently making assumptions.

Ambiguity is useful information. It identifies where further analysis or clarification is required.

## 10. Prioritise Requirements

Not every requirement has the same importance.

A simple prioritisation approach is:

| Priority | Meaning |
|---|---|
| Must have | Required for the solution to fulfil its core purpose |
| Should have | Important but not essential to the first usable version |
| Could have | Useful enhancement |
| Won't have | Outside the current scope |

Prioritisation helps define the minimum viable scope and prevents secondary features from obscuring the main user need.

For example, in LinkedIn Insights, identifying relevant connections is more central to the purpose of the application than additional visualisation features.

In Deal Compass, calculating and presenting the core financial implications of a deal is more fundamental than optional scenario enhancements.

## 11. Define Use Cases

Use cases describe how users interact with the system to achieve a goal.

A simple use case can identify:

- Actor
- Goal
- Preconditions
- Main flow
- Alternative flows
- Expected outcome

### LinkedIn Insights

**Use case: Identify relevant connections**

**Actor:** Job seeker

**Goal:** Identify connections that may be relevant to a target company or opportunity.

**Main flow:**

1. User imports connection data.
2. System processes the available information.
3. User searches for or selects a target company.
4. System identifies matching connections.
5. User reviews the results.

### Deal Compass

**Use case: Analyse an investment proposal**

**Actor:** Startup founder

**Goal:** Understand the implications of proposed investment terms.

**Main flow:**

1. User enters investment information.
2. System processes the inputs.
3. System calculates relevant values.
4. User reviews the results.
5. User compares scenarios where applicable.

Use cases provide a useful bridge between requirements and solution design.

## 12. Write User Stories

User stories express requirements from the user's perspective.

A common format is:

> As a [user], I want to [action], so that [benefit].

For example:

### LinkedIn Insights

> As a job seeker, I want to filter my connections by company so that I can identify people who may be relevant to a job opportunity.

### Deal Compass

> As a founder, I want to model the financial implications of proposed investment terms so that I can compare different scenarios.

A user story should describe the user's need rather than prescribe the technical implementation.

## 13. Define Acceptance Criteria

Acceptance criteria define how we can determine whether a requirement has been met.

For example:

**LinkedIn Insights user story**

> As a job seeker, I want to filter my connections by company so that I can identify relevant contacts.

**Acceptance criteria**

- The user can select or enter a company.
- The system displays matching connections.
- The results contain the available relevant connection information.
- If no matching connections exist, the system communicates that no results were found.

Acceptance criteria make requirements more testable and reduce ambiguity between analysis, development and validation.

## 14. Model the Solution

Diagrams can make requirements easier to understand than text alone.

Depending on the problem, useful models may include:

- Use case diagrams
- Activity diagrams
- Process workflows
- Sequence diagrams
- Data or domain models

For example:

    User
      ↓
    Import data
      ↓
    Analyse data
      ↓
    Apply criteria
      ↓
    Display results
      ↓
    User reviews results

The same approach can be applied to Deal Compass:

    Founder
       ↓
    Enter investment terms
       ↓
    Calculate results
       ↓
    Model scenarios
       ↓
    Compare results
       ↓
    Review decision-support information

The purpose of a diagram is to communicate the requirement or process clearly, not to create a diagram simply for its own sake.

The diagrams in this repository are therefore treated as part of the requirements-analysis process.

See the [`diagrams/`](../diagrams/) directory.

## 15. Use AI to Support Requirements Analysis

AI can assist with requirements analysis, particularly when working with large amounts of unstructured information.

Potential uses include:

- Structuring unstructured information
- Identifying potential requirements
- Grouping related requirements
- Identifying ambiguity
- Highlighting missing information
- Suggesting clarification questions
- Generating initial user stories
- Suggesting acceptance criteria
- Identifying relationships between requirements
- Supporting process and workflow analysis
- Reviewing requirements for consistency

For the case studies in this repository, AI can be used to support the analysis of the existing project concepts and identify areas that require further definition.

AI-generated analysis should not automatically be treated as valid requirements.

The analyst remains responsible for checking whether a proposed requirement is supported by the available information and whether it reflects the actual user or business need.

A controlled workflow might look like:

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

## 16. Validate Requirements

Requirements should be reviewed before they are used as the basis for implementation.

Useful validation questions include:

### Is it clear?

Could two people interpret the requirement differently?

### Is it necessary?

Does it support an identified user or business need?

### Is it feasible?

Can the requirement realistically be implemented within the known constraints?

### Is it testable?

Can we determine whether the requirement has been satisfied?

### Is it consistent?

Does it conflict with another requirement?

### Is it traceable?

Can the requirement be connected to the underlying business or user need?

## Requirements Analysis Checklist

    [ ] Problem is clearly defined
    [ ] Users and stakeholders identified
    [ ] Goals identified
    [ ] Functional requirements identified
    [ ] Non-functional requirements considered
    [ ] Business rules identified
    [ ] Data requirements considered
    [ ] Assumptions recorded
    [ ] Constraints identified
    [ ] Gaps and ambiguities identified
    [ ] Requirements prioritised
    [ ] Use cases identified
    [ ] User stories created where appropriate
    [ ] Acceptance criteria defined
    [ ] Relevant processes modelled
    [ ] Requirements reviewed for consistency
    [ ] Requirements validated
    [ ] AI-generated suggestions reviewed by a human

## Output

The output of requirements analysis is not simply a list of features.

It is a structured understanding of:

    Why
     ↓
    Who
     ↓
    What
     ↓
    How
     ↓
    How we know it works

For the two case studies, this analysis provides the basis for understanding the relationship between the original problem, the proposed solution and the resulting application prototype.

## Key Principle

Requirements analysis creates the connection between a problem and a solution.

> **Understand the need before defining the solution.**
