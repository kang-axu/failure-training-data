# Kang & A-Xu FTD Specification

## Failure Training Data for Human-AI Systems

**Version:** 0.1  
**Status:** Experimental  
**Origin:** China, 2026

---

## 1. Purpose

This document defines the experimental **Kang & A-Xu FTD Specification**.

FTD stands for **Failure Training Data**.

The phrase "failure training data" predates this project and has been used in other technical contexts.

This specification does **not** claim to have invented those words.

Within this specification, FTD refers to a structured operational record designed to help human-AI systems convert failures into reusable organizational experience.

The core lifecycle is:

`FAILURE → HUMAN CORRECTION → VALIDATION → BEHAVIORAL UPDATE`

The purpose of FTD is not merely to remember that something failed.

The purpose is to make future behavior change because the failure happened.

---

## 2. Core Definition

Within the Kang & A-Xu FTD Specification:

> **FTD is a structured record of failure, human correction, real-world validation, and behavioral update.**

A failure record is not complete FTD merely because the failure was documented.

Meaningful experience should allow the system to trace:

1. what was attempted
2. what failed
3. why a human rejected or corrected it
4. what correction was made
5. how the correction was tested
6. what reality showed
7. what future behavior should change

---

## 3. Minimum FTD Lifecycle

An FTD record SHOULD progress through four stages.

### Stage 1 — Failure

A meaningful gap exists between:

- expected result
- actual result

The failure should be observable and describable.

---

### Stage 2 — Human Correction

A human identifies that the original result is unacceptable, incomplete, inefficient, unsafe, or otherwise unsuitable.

The correction should record:

- what the human rejected
- why it was rejected
- what decision was made
- what changed

Human disagreement alone does not prove that the human correction is correct.

A human correction initially creates a hypothesis to be tested.

---

### Stage 3 — Validation

The correction is tested against reality.

Validation may include:

- real production use
- measurable performance
- human acceptance
- user response
- repeated task execution
- operational outcomes
- other observable evidence

Without validation, the lesson remains uncertain.

---

### Stage 4 — Behavioral Update

The validated lesson changes future behavior.

The update may affect:

- a human procedure
- an AI instruction
- an agent role
- a prompt
- a workflow
- a quality gate
- a routing rule
- a tool-selection rule
- an automation
- another operational policy

If nothing changes next time, organizational learning has not yet occurred.

---

## 4. Experience Rule Lifecycle

FTD uses three rule states.

### R0 — Hypothesis

A lesson inferred from a failure and its correction.

It has not yet earned default operational use.

A single failure MUST NOT automatically become a permanent production rule.

---

### R1 — Candidate Experience

The correction has worked again in one or more sufficiently similar real situations.

The lesson now has evidence of reuse.

It may guide future work but remains open to further validation.

---

### R2 — Production Rule

The lesson has survived repeated real-world validation within a defined scope.

At this stage, relevant humans or AI agents may follow it by default.

An R2 rule is still not permanent truth.

If later evidence contradicts it, the rule should be reviewed, downgraded, modified, or retired.

> **Reality has final authority.**

---

## 5. Minimum FTD Record

An FTD record SHOULD contain the following fields.

### 5.1 Identity

```text
ftd_id:
project:
task:
created_at:
owner:
status:
```

---

### 5.2 Original Attempt

```text
input:
expected_result:
actual_output:
```

---

### 5.3 Human Judgment

```text
human_rejection_reason:
human_decision:
```

The rejection reason SHOULD describe the actual judgment.

Avoid records such as:

```text
bad
wrong
not good enough
```

without further explanation.

---

### 5.4 Failure Diagnosis

```text
observed_failure:
root_cause_hypothesis:
```

A root-cause hypothesis MUST remain distinguishable from a validated cause.

---

### 5.5 Correction

```text
correction_action:
corrected_output:
```

---

### 5.6 Validation

```text
validation_method:
validation_result:
validation_count:
evidence:
```

---

### 5.7 Scope

```text
applies_to:
does_not_apply_to:
```

Every reusable lesson should define where it applies.

A useful rule without a scope can easily become a harmful rule.

---

### 5.8 Experience Lifecycle

```text
rule_status:
```

Allowed values:

```text
R0 — Hypothesis
R1 — Candidate Experience
R2 — Production Rule
```

---

### 5.9 Behavioral Update

```text
future_behavior_change:
agents_or_roles_affected:
```

This section is essential.

If the record cannot explain how future behavior changes, it is not yet complete organizational learning.

---

## 6. FTD Validity Rules

### Rule 1

**Failure documentation alone is not FTD.**

A log of what went wrong is history.

---

### Rule 2

**Human correction alone is not confirmed experience.**

A human judgment creates a candidate correction, not automatic truth.

---

### Rule 3

**No validation means no confirmed experience.**

A correction must face reality.

---

### Rule 4

**No behavioral update means no organizational learning.**

If the next attempt behaves exactly as if the failure never happened, the experience was not successfully inherited.

---

### Rule 5

**One failure must not automatically create a permanent rule.**

The default state of a lesson from a single failure is:

`R0 — Hypothesis`

---

### Rule 6

**Scope must be preserved.**

A rule that works in one context must not automatically be generalized to all contexts.

---

### Rule 7

**Contradictory evidence must be retained.**

FTD should not preserve only evidence that supports an existing rule.

If reality contradicts an R1 or R2 rule, that contradiction is itself valuable FTD.

---

## 7. Evidence Principle

FTD should distinguish among:

- observation
- human judgment
- hypothesis
- correction
- validation
- production rule

These are not the same thing.

For example:

> "We believe the opening revealed the conclusion too early."

is a hypothesis.

It becomes stronger only after later production and validation provide evidence.

FTD should preserve this distinction.

---

## 8. Portability Principle

FTD should describe experience independently of one specific AI vendor or tool whenever possible.

Validated experience should survive changes in:

- models
- agents
- software
- automation tools
- workflows
- organizations

The implementation may change.

The experience should remain transferable.

---

## 9. Human Role

FTD assumes that humans may contribute forms of judgment that are difficult to capture directly in system metrics.

Examples include:

- taste
- quality judgment
- business judgment
- contextual understanding
- risk tolerance
- strategic choice

FTD should not reduce human judgment to an unexplained approval or rejection.

When possible, it should capture:

> **Why did the human change the system's decision?**

That explanation may become future organizational experience.

---

## 10. AI Role

AI systems may assist with:

- detecting failures
- organizing evidence
- proposing root causes
- comparing cases
- suggesting corrections
- retrieving previous FTD
- applying validated rules
- identifying possible contradictions

However, an AI-generated explanation is not automatically validated experience.

The same lifecycle still applies:

`FAILURE → HUMAN CORRECTION → VALIDATION → BEHAVIORAL UPDATE`

---

## 11. Self-Application

FTD itself is subject to FTD.

If real use shows that part of this specification is wrong, incomplete, or harmful:

1. record the failure
2. document the correction
3. validate the change
4. update future versions

The specification must be capable of learning from its own failures.

> **FTD should be able to learn from its own failures.**

---

## 12. Scope, Prior Art, and Rights

The phrase **"failure training data"** existed before this project and has been used in other technical contexts.

This project does **not** claim to have coined or invented that phrase.

The terms **"Human-AI OS"** and **"Human-AI Operating System"** have also been used independently by other projects and authors.

This project does **not** claim ownership of those terms.

FTD v0.1 is presented as an **experimental specification**, not as an established or officially recognized industry standard.

These acknowledgements should not be interpreted as a waiver of any rights that may lawfully exist in original materials associated with this project, including its:

- original written expression
- documentation
- case materials
- software
- datasets
- visual identity
- brand identifiers
- commercial implementations
- or other protectable intellectual property

Except for permissions necessarily provided under GitHub's Terms of Service or required by applicable law, publication of this repository does not by itself grant an additional license to use, reproduce, distribute, modify, commercialize, or sublicense project materials.

No separate open-source or content license has been granted unless one is explicitly added in writing.

The project may later be developed into commercial forms including, but not limited to:

- software
- enterprise systems
- consulting
- implementation services
- training
- education
- certification
- data products
- agent systems
- evaluation systems
- other FTD-related products or services

The purpose of this section is not to claim ownership over ideas or terminology that predate this project.

Its purpose is to distinguish prior terminology from the specific materials, implementations, identity, and future work developed through this project.

---

## 13. Design Goal

The long-term design goal is simple:

> **A human-AI system should become better not only because its model improved, but because its past failures were not wasted.**

Or, more operationally:

> **We do not optimize for being right the first time.  
> We optimize for not paying for the same mistake twice.**

---

## 14. Origin

This project began in **China in 2026**.

FTD emerged while Zhang Kang (康哥) and A-Xu (阿序) were working through real business, content-production, and human-AI collaboration failures.

Again and again, the same question appeared:

> **How can a human-AI system avoid paying for the same mistake twice?**

FTD did not begin as a claim of theoretical novelty.

It began as an operational need.

---

## 15. Specification Status

```text
Specification: Kang & A-Xu FTD
Version: 0.1
Status: Experimental
Year: 2026
Origin: China
```

Future versions should preserve a visible history of:

- what changed
- why it changed
- what evidence caused the change

---

## Philosophy

> **We do not optimize for being right the first time.  
> We optimize for not paying for the same mistake twice.**

A human-AI organization should not improve only because it gained access to a stronger model.

It should also improve because:

> **Its failures were not wasted.**

---

## Project Identity

**Kang & A-Xu**

A project initiated by **Zhang Kang (康哥)**, developed with **A-Xu (阿序)**, an AI collaborator.

Copyright © 2026 Zhang Kang
