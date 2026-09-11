# AI Requirements Analyst

## Requirements Analysis with AI-Assisted Workflows

A portfolio project exploring how AI can support requirements analysis, from understanding a business problem through to structured requirements, use cases, workflows and solution modelling.

The project uses two existing application prototypes as case studies:

- **LinkedIn Insights** — an AI-assisted tool for analysing a LinkedIn network during a job search
- **Deal Compass** — an AI-assisted tool for analysing key terms in a proposed startup investment

The prototypes are maintained in their own repositories. This repository focuses on the **requirements analysis and solution-design perspective** behind those projects.

## What this project demonstrates

The project explores how to:

- Analyse a business problem before defining a solution
- Identify users, stakeholders and their goals
- Translate business needs into structured requirements
- Separate functional and non-functional requirements
- Identify assumptions, dependencies and information gaps
- Define use cases and user interactions
- Develop user stories and acceptance criteria
- Model processes and system behaviour
- Use diagrams to communicate requirements
- Use AI to support requirements analysis
- Apply human judgement to validate AI-assisted outputs

## Case Studies

### LinkedIn Insights

An existing prototype that turns a LinkedIn connection export into actionable information for job searching.

The requirements analysis explores questions such as:

- Who are the intended users?
- What problem are they trying to solve?
- What information do they need?
- How should connection data be organised?
- How can relevant contacts be identified?
- What should the system allow the user to do?

See [`case studies/linkedin-insights.md`](case-studies/linkedin-insights.md).

**Prototype:** See the [LinkedIn Insights repository](https://github.com/Elly11Nov/linkedin-buddy-dash).

### Deal Compass

An existing prototype designed to help startup founders understand and compare key terms in a proposed investment.

The requirements analysis explores questions such as:

- What information does the founder need to provide?
- What calculations and business rules are required?
- Which investment terms need to be represented?
- How should scenarios be presented?
- What information supports decision-making?

See [Deal Compass case study](case%20studies/deal-compass.md)
**Prototype:** See the [Deal Compass repository](https://github.com/Elly11Nov/term-sheet-ninja).

## Requirements Analysis Approach

The analysis follows a structured process:

    Business problem
          ↓
    Users and stakeholders
          ↓
    Goals and needs
          ↓
    Requirements
          ↓
    Use cases and user stories
          ↓
    Processes and system behaviour
          ↓
    Data and business rules
          ↓
    Acceptance criteria
          ↓
    Solution modelling
          ↓
    Validation

The exact techniques used depend on the problem being analysed.

## AI-Assisted Requirements Analysis

AI can support requirements analysis by helping to:

- Structure unstructured information
- Identify potential requirements
- Highlight ambiguity
- Identify missing information
- Suggest questions for clarification
- Generate initial user stories
- Suggest acceptance criteria
- Identify relationships between requirements
- Support analysis of processes and workflows
- Review requirements for consistency

AI-generated analysis is treated as an input to the process, not as the final source of truth.

Human review remains necessary to validate requirements, resolve ambiguity and confirm that the proposed solution reflects the actual business need.

## Diagrams

The repository includes diagrams created as part of the requirements-analysis process.

The diagrams are used to communicate different aspects of the proposed solution, rather than simply to illustrate the finished application.

Examples may include:

- Use case diagrams
- Activity diagrams
- Process workflows
- Sequence diagrams
- Domain or data models

See the [`diagrams/`](diagrams/) directory.

## From Requirements to Prototype

The relationship between this repository and the existing application projects can be viewed as:

    Business problem
          ↓
    Requirements analysis
          ↓
    Use cases and models
          ↓
    Solution definition
          ↓
    Prototype
          ↓
    Validation and iteration

The LinkedIn Insights and Deal Compass repositories contain the resulting application prototypes.

This repository focuses on the analysis and definition that sits behind the solution.

## My Role

Requirements analysis, problem definition, information architecture, user and stakeholder analysis, functional requirements, process modelling, use cases, acceptance criteria, documentation and AI-assisted solution analysis.

The application prototypes were developed using AI-assisted development tools. The focus of this repository is not software development itself, but the analysis and definition of what the solution should do and how it should work.

## Repository Structure

```text
AI-Requirements-Analyst/
├── README.md
├── docs/
│   ├── requirements-analysis.md
│   ├── requirements-engineering-approach.md
│   └── ...
├── case-studies/
│   ├── linkedin-insights.md
│   └── deal-compass.md
└── diagrams/
    ├── linkedin-insights-use-case.svg
    ├── linkedin-insights-workflow.svg
    ├── deal-compass-use-case.svg
    └── deal-compass-workflow.svg# AI-Requirements-Analyst
