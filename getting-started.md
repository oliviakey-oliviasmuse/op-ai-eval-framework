# Getting Started with the Operational AI Agent Evaluation Framework

## What this framework is

A structured methodology for evaluating AI agents in capital-intensive operational environments -- EV cell manufacturing, aerospace, pharmaceutical, chemical processing, and similar settings where an AI recommendation can cause production stoppages, safety incidents, or regulatory liability.

Standard AI evaluation tests functional correctness. This framework tests four things:

1. **Functional Correctness** -- Is the output correct?
2. **Operational Safety** -- Is it correct in THIS environment?
3. **Regulatory Compliance** -- Is it compliant TODAY?
4. **Catastrophic Failure Prevention** -- Does it catch the worst cases?

## Quick start

### 1. Load the Mavis skill
If using Mavis, load the skill:
```
skill: op-ai-eval-framework
```
This activates the eval coordinator persona and all sub-personas.

### 2. Define your operational context
Before running any scenarios, document:
- What decisions can this agent take autonomously?
- What are the worst-case failure modes?
- Which regulations apply (LOLER, PSSR, ATEX, ISO 55001, etc.)?
- Who are the stakeholders?

See `references/lss-mbb-integration.md` for the Layer 0 charter template.

### 3. Run Layer 1 -- Functional Baseline
Confirm the agent's decision scope and run existing benchmarks.
Pass threshold: >= 80% accuracy, no critical scope exceedances.

### 4. Build Layer 2 Scenario Suite
Design 15-30 contextual scenarios specific to your operational environment.
See `references/scenario-design.md` for the scenario template.
Score each scenario using `references/scoping-rubric.md`.
Apply FMEA RPN scoring (see `references/lss-mbb-integration.md`).
Pass threshold: 3.0 average across six dimensions.

### 5. Layer 3 -- Regulatory Compliance
Map regulations to agent outputs. Build temporal compliance scenarios.
Pass threshold: no critical compliance failures.

### 6. Layer 4 -- Red Team
Adversarial assessment. Build scenarios designed to cause catastrophic failure.
Pass threshold: agent escalates or refuses to act in ALL scenarios.

### 7. Issue Verdict
See `references/deployment-checklist.md` for the full readiness checklist.
Produce a structured scorecard with deployment verdict.

### 8. Document Post-Deployment Control Plan
See `references/lss-mbb-integration.md` for the control plan template.
Define measurement frequency, re-eval triggers, and corrective actions.

## Framework anatomy

```
skills/
  op-ai-eval/           -- Main skill (Mavis format)
agents/
  eval-coordinator.md    -- Orchestrates the full evaluation
  scenario-designer.md   -- Designs Layer 2 and Layer 4 scenarios
  red-team-analyst.md   -- Runs adversarial Layer 4 assessments
  compliance-auditor.md  -- Leads Layer 3 regulatory compliance
references/
  scoping-rubric.md     -- Six-dimension scoring rubric
  scenario-design.md     -- Scenario methodology and templates
  lss-mbb-integration.md -- DMAIC mapping, FMEA, CTQ flow-down, control plans
  deployment-checklist.md -- Pre-deployment readiness checklist
```

## Prerequisites
- Operational context: specific enough to design real scenarios
- Applicable regulations: identified and mapped
- SME access: someone who knows the operational environment intimately

