# Flexdoc Property Decision Engine

This repository contains the core decision engine used by Flexdoc to assess property investment scenarios.

It is designed to support self made and aspirational investors by turning messy inputs into clear, explainable outcomes.

The engine does not give financial advice.  
It produces structured decision signals to support human judgement.

---

## What this engine does

The decision engine evaluates a property scenario and produces:

- A consolidated decision score  
- Key risk and strength signals  
- Reason codes explaining why the score moved up or down  
- A structured output that can be audited, logged, and reviewed  

The goal is clarity, not prediction.

---

## What it is used for

- Pre screening property deals  
- Comparing multiple acquisition scenarios  
- Supporting broker and adviser conversations  
- Powering internal Flexdoc tools and workflows  

This engine is opinionated by design.  
It reflects Flexdoc’s view of risk, structure, and capital efficiency.

---

## How it works

Inputs are provided as structured data.  
Each module evaluates a specific dimension of the deal.

Typical dimensions include:

- Borrower structure and income quality  
- Asset type and location risk  
- Leverage and serviceability pressure  
- Cash flow resilience  
- Execution and complexity risk  

Each dimension contributes weighted signals to a final score.  
All weights and signals are explicit.

No black boxes.

---

## Inputs

Inputs are provided as JSON objects.

A typical input includes:

- Borrower profile  
- Property details  
- Loan structure  
- Assumptions used  

See the `examples/` directory for sample inputs.

---

## Outputs

The engine returns a structured result containing:

- Overall score  
- Decision band, for example strong, borderline, high risk  
- Contributing factors with weights  
- Human readable reason codes  

Outputs are deterministic and reproducible.

---

## Project structure

```text
flexdoc-property-decision-engine/
├── config/        # Configuration, weights, thresholds, rule definitions
├── docs/          # Decision framework, schemas, and design notes
├── engine/        # Core scoring and decision logic
├── examples/      # Sample inputs and expected outputs
├── test/          # Unit tests and scenario tests
├── .gitignore
└── README.md
```

---

## Design principles

- Explainability over complexity  
- Deterministic outputs  
- Clear separation between data, rules, and logic  
- Human in the loop by default  

This engine is a decision support system, not an automated approval tool.

---

## Running the engine

Basic usage follows this pattern:

1. Prepare a JSON input  
2. Pass it to the decision engine  
3. Receive a structured score and explanation  

Detailed run instructions will be added as the CLI and API stabilise.

---

## Status

This project is under active development.

Interfaces may evolve.  
The core philosophy will not.

---

## Ownership

Built and maintained by Flexdoc Labs.

Internal use first.  
External access by design, when ready.
