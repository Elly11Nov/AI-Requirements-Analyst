# Deal Compass — Requirements Analysis Case Study

## Overview

**Deal Compass** is an AI-assisted prototype designed to help startup founders assess key terms in a proposed seed investment.

The prototype translates information from a term sheet into a structured decision-support experience, allowing a founder to explore financial and governance implications and compare scenarios.

This case study applies a requirements-engineering approach to the project.

The purpose is to demonstrate how a business problem can be analysed and translated into requirements, business rules, user interactions and acceptance criteria before or alongside solution development.

The working prototype is maintained in the [Deal Compass repository](https://github.com/Elly11Nov/term-sheet-ninja).

---

## 1. The Problem

Early-stage investment term sheets can contain several financial and governance provisions that need to be considered together.

A founder may need to understand questions such as:

- How much money is being invested?
- What is the implied post-money valuation?
- What percentage of the company will the investor own?
- How much funding does the company still need?
- How do different terms affect founder ownership?
- What happens under different investment or exit scenarios?
- What governance or control provisions are included?

Looking at individual terms in isolation does not necessarily provide a clear picture of the overall deal.

### Problem statement

> A founder needs a structured way to understand and compare the financial and governance implications of a proposed investment.

The problem is therefore not simply to calculate individual values.

The solution needs to bring related information together so that the founder can understand the overall implications of the proposed deal.

---

## 2. User

### Primary user

**Startup founder**

The founder is evaluating a proposed investment and needs to understand the implications of the terms before making decisions or entering negotiations.

### User goal

> Understand and compare the implications of proposed investment terms.

The prototype is designed around this goal rather than around the mechanics of a particular interface.

---

## 3. Business Objectives

The solution should help the user:

- Understand the financial implications of an investment
- Identify the resulting ownership position
- Explore important deal terms
- Compare different scenarios
- Identify areas that may require further consideration or negotiation

The prototype is intended as a decision-support tool.

It is not intended to replace legal, financial or investment advice.

---

## 4. Scope

### In scope

The prototype considers:

- Investment amount
- Valuation
- Investor ownership
- Founder ownership
- Funding gap
- Liquidation preference
- Vesting
- Board and control provisions
- Anti-dilution structures
- Investment tranches
- Milestone-based scenarios
- Exit-value scenarios

### Out of scope

The prototype does not attempt to:

- Provide legal advice
- Provide regulated investment advice
- Replace professional financial analysis
- Negotiate directly with investors
- Connect to external investment platforms
- Automatically determine whether a deal should be accepted

The scope is focused on **decision support and scenario analysis**.

---

## 5. Functional Requirements

The requirements can be grouped into several areas.

### Input requirements

The system should allow the user to provide the information required to analyse the proposed investment.

This includes relevant financial and deal terms.

### Calculation requirements

The system should calculate values derived from the user's inputs.

Examples include:

- Post-money valuation
- Investor ownership
- Founder ownership
- Funding gap

### Deal-term requirements

The system should allow relevant investment terms to be represented, including:

- Liquidation preference
- Vesting
- Board and control provisions
- Anti-dilution provisions
- Tranches
- Milestones

### Scenario requirements

The system should allow different assumptions or investment scenarios to be modelled and compared.

### Output requirements

The system should present the resulting information in a form that allows the founder to understand and compare the implications of the proposed deal.

---

## 6. Non-Functional Considerations

The requirements analysis also considers qualities of the user experience.

### Clarity

Financial and deal information should be presented in a way that is understandable without requiring the user to interpret raw calculations.

### Usability

The user should be able to enter information, review results and explore scenarios without unnecessary complexity.

### Consistency

The same terminology and calculation concepts should be used consistently throughout the application.

### Transparency

Calculated values should be understandable and traceable to the information provided by the user.

### Maintainability

Business rules and calculations should be structured so that they can be reviewed and changed independently of the presentation layer.

---

## 7. Data Requirements

The solution works with several categories of information.

### Investment

- Investment amount
- Valuation
- Ownership

### Founder

- Founder ownership
- Ownership after investment

### Deal terms

- Liquidation preference
- Vesting
- Board/control provisions
- Anti-dilution structure

### Funding

- Company funding requirement
- Proposed investment
- Funding gap

### Scenarios

- Investment assumptions
- Milestones
- Tranches
- Exit values

A simplified information model is:

    Investment
        ├── Amount
        ├── Valuation
        └── Ownership
              │
              ├── Investor
              └── Founder

    Deal Terms
        ├── Liquidation preference
        ├── Vesting
        ├── Board / control
        └── Anti-dilution

    Scenarios
        ├── Tranches
        ├── Milestones
        └── Exit value

---

## 8. Business Rules

Some of the requirements depend on financial calculations and relationships between inputs.

For example:

    Investment amount
            +
    Pre-money valuation
            ↓
    Post-money valuation
            ↓
    Investor ownership
            ↓
    Founder ownership

The requirements analysis therefore needs to distinguish between:

- User-provided values
- Calculated values
- Business rules
- Displayed results

This distinction is important because a calculation is not simply a user-interface feature.

It represents business logic that should be defined, reviewed and tested.

---

## 9. Use Case

### Analyse an Investment Proposal

**Actor:** Startup founder

**Goal:** Understand the financial and deal implications of a proposed investment.

### Preconditions

- The founder has information about the proposed investment.
- The required inputs are available.
- The founder can enter the relevant deal terms.

### Main flow

1. The founder enters the investment information.
2. The system validates the available inputs.
3. The system calculates the relevant financial values.
4. The founder enters or reviews additional deal terms.
5. The system presents the resulting information.
6. The founder reviews the implications of the proposed deal.
7. The founder can model different scenarios where supported.
8. The founder compares the resulting scenarios.

### Alternative flow

If required information is missing or invalid:

1. The system identifies the problematic input.
2. The user is prompted to correct or complete the information.
3. The analysis continues once the required information is valid.

---

## 10. User Stories

### Investment analysis

> As a founder, I want to enter the proposed investment terms so that I can understand the financial implications of the deal.

### Ownership analysis

> As a founder, I want to see the ownership implications of an investment so that I can understand how the proposed deal affects founder and investor ownership.

### Scenario analysis

> As a founder, I want to compare different investment scenarios so that I can understand how changes to the proposed terms affect the outcome.

### Deal-term analysis

> As a founder, I want to capture important investment terms so that I can consider financial and governance provisions together.

---

## 11. Acceptance Criteria

### Investment analysis

- The user can enter the relevant investment information.
- The system uses the entered values in the applicable calculations.
- Calculated results are displayed to the user.
- The results are presented using understandable terminology.

### Ownership analysis

- The system calculates the relevant ownership values.
- The founder and investor positions are distinguishable.
- The resulting ownership information can be reviewed by the user.

### Scenario analysis

- The user can define supported scenario variations.
- The system calculates the resulting values for each scenario.
- The user can compare the resulting scenarios.

### Deal-term analysis

- The user can capture the supported deal terms.
- The selected terms are reflected in the analysis.
- Terms that require further interpretation or professional advice are not presented as definitive legal conclusions.

---

## 12. Assumptions and Constraints

Requirements analysis distinguishes between known information, assumptions and constraints.

### Known

- The prototype is designed for startup founders.
- The prototype analyses investment terms.
- The prototype includes financial calculations and scenario analysis.
- The prototype includes several financial and governance terms.

### Assumptions

- The user has access to the relevant information from the proposed investment.
- The user understands the basic context of the investment being analysed.
- The information entered by the user is sufficiently accurate for the calculations being performed.

### Constraints

- The prototype is decision-support software rather than professional financial or legal advice.
- The prototype does not replace professional review of investment documentation.
- The quality of the results depends on the quality of the information entered.

Making these distinctions explicit helps prevent assumptions from being mistaken for requirements.

---

## 13. Potential Gaps and Questions

A requirements analysis should also identify areas that may require further clarification.

Examples include:

- Which additional investment structures should be supported?
- Which jurisdiction-specific rules might affect the calculations?
- Which additional governance provisions should be represented?
- How should complex cap-table structures be handled?
- How should multiple investment rounds be represented?
- What level of scenario modelling would be required in a production system?
- What data should be persisted between sessions?
- What security requirements would apply to sensitive financial information?

These questions are deliberately not resolved by assumption.

They represent areas for further requirements elicitation if the prototype were developed into a production solution.

---

## 14. Prioritisation

A possible prioritisation for an initial version is:

| Priority | Requirement |
|---|---|
| Must have | Capture core investment information |
| Must have | Calculate key ownership and valuation values |
| Must have | Present the resulting financial information |
| Should have | Capture important deal terms |
| Should have | Support scenario comparison |
| Could have | Additional scenario and exit modelling |
| Could have | Additional visualisations |
| Won't have | Automated legal or investment advice |

This prioritisation keeps the core purpose of the application clear while allowing additional functionality to be considered later.

---

## 15. AI-Assisted Analysis

AI can support the requirements process by helping to structure and review information.

For this case study, potential AI-assisted activities include:

- Extracting potential requirements from an initial problem description
- Identifying missing information
- Suggesting clarification questions
- Grouping requirements into logical categories
- Identifying relationships between requirements
- Suggesting user stories
- Suggesting acceptance criteria
- Reviewing requirements for ambiguity or inconsistency

AI output is treated as a source of suggestions rather than as validated requirements.

For example:

    Initial problem
          ↓
    AI-assisted analysis
          ↓
    Potential requirements
          ↓
    Human review
          ↓
    Validated requirements

The analyst remains responsible for deciding whether a requirement is relevant, accurate and supported by the available information.

---

## 16. Requirements to Prototype

The relationship between the requirements analysis and the existing prototype can be represented as:

    Founder problem
          ↓
    Requirements analysis
          ↓
    User stories
          ↓
    Business rules
          ↓
    Acceptance criteria
          ↓
    Solution design
          ↓
    Prototype

The existing Deal Compass prototype represents the solution-design and implementation stage of this process.

This repository focuses on the analysis that provides the foundation for the solution.

---

## 17. Validation

The requirements should be validated against the intended user outcome.

Key questions include:

- Does the solution address the founder's actual problem?
- Are the calculations based on clearly defined rules?
- Are important inputs represented?
- Can the user understand the resulting information?
- Can different scenarios be compared where required?
- Are assumptions clearly identified?
- Are unsupported conclusions avoided?
- Can the requirements be tested?

Validation should involve both requirements review and review of the resulting prototype.

A prototype can expose requirements that were unclear or incomplete during the initial analysis.

---

## 18. Requirements Traceability

A simplified traceability chain is:

    Founder need
          ↓
    Requirement
          ↓
    User story
          ↓
    Business rule
          ↓
    Acceptance criteria
          ↓
    Prototype behaviour
          ↓
    Validation

This provides a connection between the original problem and the resulting functionality.

It also makes it easier to understand why a feature exists and what requirement it is intended to satisfy.

---

## Conclusion

Deal Compass demonstrates how a complex business problem can be broken down into user needs, requirements, business rules, data requirements, use cases and acceptance criteria.

The analysis also shows where AI can assist with requirements work while keeping human validation in the process.

The overall approach is:

    Understand the problem
            ↓
    Identify the user
            ↓
    Define the goal
            ↓
    Analyse requirements
            ↓
    Identify business rules
            ↓
    Model the solution
            ↓
    Define acceptance criteria
            ↓
    Validate
            ↓
    Iterate

The objective is not to define every detail before development begins.

It is to create enough structure and clarity to ensure that the solution addresses the right problem and that its behaviour can be understood and validated.

> **Good requirements connect the user's need to the behaviour of the solution.**

---

## Related Work

- [Deal Compass prototype](https://github.com/Elly11Nov/term-sheet-ninja)
- [Requirements Analysis](../docs/requirements-analysis.md)
- [Requirements Engineering Approach](../docs/requirements-engineering-approach.md)
- [LinkedIn Insights case study](linkedin-insights.md)

## Portfolio Note

This case study is based on my own application prototype and is presented as a portfolio example of requirements analysis and solution modelling.

The financial concepts represented in the prototype are for demonstration and decision-support purposes and should not be interpreted as legal, financial or investment advice.
