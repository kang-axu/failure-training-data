# Failure Training Data (FTD)

> **Failure → Human Correction → Verification → Behavior Update**

FTD is a public, experimental framework for describing how human-AI systems can turn a failure into a reusable lesson without confusing an untested correction with a production rule.

## Public Scope

This repository explains the public methodology:

- a failure is observed
- a human correction is recorded
- the correction is verified against reality
- future behavior can be updated when evidence supports it

The R0, R1, and R2 states distinguish a hypothesis, a candidate experience, and a validated production rule.

## Public Materials Only

**Public FTD repository contains framework documentation, sanitized examples, and teaching templates only. Internal failure records, prompts, correction logic, validation datasets, and derived production rules are not part of the public repository.**

No real project record, original input chain, internal correction output, or production-learning asset should be added here without passing the data and case policy.

## Sanitized Examples

Sanitized teaching examples may be added in the future. They will be historical, synthetic, or otherwise de-identified examples designed to explain the framework without exposing internal operating assets.

## Status

FTD v0.1 is an experimental public framework. It is not a complete internal operating system or a claim that an unverified lesson should become a permanent rule.

See [FTD-SPEC.md](FTD-SPEC.md), [FTD-TEMPLATE.md](FTD-TEMPLATE.md), [PUBLIC-BOUNDARY.md](PUBLIC-BOUNDARY.md), and [DATA-AND-CASE-POLICY.md](DATA-AND-CASE-POLICY.md).
