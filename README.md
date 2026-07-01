# Operational AI Agent Evaluation Framework

> A framework for evaluating AI agents in capital-intensive operational environments — beyond functional correctness to operational safety, regulatory compliance, and catastrophic failure prevention.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## The Problem

AI agents pass every benchmark. They still cause catastrophic failures in production environments.

Standard AI evaluation focuses on functional correctness. But in capital-intensive operational environments, correctness is the floor, not the ceiling.

An agent that recommends a maintenance action without checking whether the regulation changed six months ago is correct and dangerous. Standard benchmarks miss this.

## What This Framework Does

Evaluates AI agents across four dimensions:

1. Functional Correctness — Does the agent do the right thing?
2. Operational Safety — Does it do the right thing in your specific operational context?
3. Regulatory Compliance — Does the output align with current regulatory requirements?
4. Catastrophic Failure Prevention — Does it catch the worst cases?

## The Four-Layer Architecture

| Layer | Question | Method |
|---|---|---|
| Layer 1 | Is the output correct? | Benchmark datasets, unit tests |
| Layer 2 | Is it correct in this environment? | Contextual scenario suite |
| Layer 3 | Is it compliant today? | Compliance audit scenarios |
| Layer 4 | Does it catch the worst cases? | Red-team adversarial scenarios |

An agent must pass all four layers. Passing layer one is not sufficient for deployment.

## Six Evaluation Dimensions

Scope Alignment | Constraint Respect | Uncertainty Handling | Temporal Awareness | Failure Mode Detection | Regulatory Currency

A score of 1-5 on each dimension. Layer pass threshold: 3.0 average.

## Quick Start

1. Define your operational context
2. Build your scenario suite (templates in references/)
3. Run evaluation with the Mavis skill
4. Interpret results against the scoring rubric

## File Structure

- SKILL.md — Mavis skill for running evaluations
- references/scoping-rubric.md — Six-dimension scoring rubric
- references/scenario-design.md — How to write eval scenarios
- references/framework-architecture.md — Four-layer architecture detail

## Status

Active development. Framework v0.1 deployed in production EV cell manufacturing environments.

## Contributing

See CONTRIBUTING.md. Improvements, scenario templates, and domain-specific extensions welcome.

## License

MIT
