# Failure Training Data (FTD)

## Kang & A-Xu FTD Specification

> **We don't just store what worked.  
> We preserve what failed, why it failed, how humans corrected it, whether the correction survived reality, and how future behavior should change.**

**A project initiated by Zhang Kang (康哥), developed with A-Xu (阿序), an AI collaborator.**

---

## What is FTD?

FTD stands for **Failure Training Data**.

The phrase "failure training data" predates this project and has been used in other technical contexts.

**This project does not claim to have coined those words.**

In this project, we define FTD for human-AI systems as:

> **A structured record of failure, human correction, real-world validation, and behavioral update.**

The core lifecycle is:

`FAILURE → HUMAN CORRECTION → VALIDATION → BEHAVIORAL UPDATE`

A failure log records what happened.

FTD asks a different question:

> **Because this failure happened, will the next attempt behave differently?**

If not, the system has preserved history.

It has not yet preserved experience.

---

## Why FTD?

Most AI systems are already capable of preserving:

- successful outputs
- prompts
- documents
- workflows
- final answers
- logs and histories

But:

> **A final answer is not the same as experience.**

Real experience also contains questions such as:

- What was attempted?
- What failed?
- Why did a human reject the result?
- What did the human change?
- Did the correction actually work?
- Was the correction validated again?
- Should future humans or AI agents behave differently because of it?

FTD is not intended to become an archive of mistakes.

Its purpose is to turn failures into **reusable organizational experience**.

---

## Core Definition

> **FTD is a structured record of failure, human correction, real-world validation, and behavioral update.**

A failure does not become meaningful FTD merely because it was documented.

It must progress through:

`FAILURE → HUMAN CORRECTION → VALIDATION → BEHAVIORAL UPDATE`

No validation means there is no confirmed experience.

No behavioral update means there is no organizational learning.

---

## Experience Rule Lifecycle

Within this specification, we use a three-stage lifecycle for lessons derived from failure.

### R0 — Hypothesis

A lesson inferred from one failure.

It may explain what went wrong, but it is **not yet a production rule**.

One failure should not automatically create a permanent organizational rule.

---

### R1 — Candidate Experience

The correction has worked again in a similar real situation.

The lesson now has evidence of reuse and may be valuable beyond the original case.

It should still remain open to further validation.

---

### R2 — Production Rule

The rule has survived repeated real-world validation.

At this stage, humans and AI agents may follow it by default within its defined scope.

> **Reality has final authority.**

Not the human.

Not the AI.

Not the model.

The result in reality does.

---

## Human-AI Systems

FTD is being developed by Kang & A-Xu as a proposed learning primitive for human-AI systems.

A human-AI system should not only automate work.

It should also be able to preserve validated experience across changes in:

- models
- tools
- agents
- workflows

> **Automation executes work.  
> Experience changes how the next work is done.**

Models will change.

Tools will change.

Agents will change.

Workflows will change.

Validated experience should be able to survive them.

---

## First Real Case

Our first FTD case comes from a real AI-assisted media production failure:

**CASE-001 — Hypit V3**

Hypit V3 reached technical completion as a finished video.

However, it failed the human editor's final quality review and was never published.

**Technically completed.**

**Editorially rejected.**

Instead of deleting the failed output, we will preserve and study:

- the original inputs
- production decisions
- rejected output
- human rejection reasons
- root-cause hypotheses
- correction actions
- corrected outputs
- later validation
- any rule that eventually survives repeated real production

The case begins at:

**Rule Status: R0 — Hypothesis**

A single failure does not justify a permanent production rule.

---

## Scope and Prior Art

The words **"failure training data"** existed before this project and have been used in other technical contexts, including machine learning and failure-related prediction or analysis.

This project does **not** claim to have invented those words.

The terms **"Human-AI OS"** and **"Human-AI Operating System"** have also been used independently by other projects and authors.

This project does **not** claim ownership of those terms.

Our focus is narrower:

**Kang & A-Xu FTD Specification** documents an operational framing for human-AI systems in which a failure becomes reusable organizational experience only when it progresses through:

`FAILURE → HUMAN CORRECTION → VALIDATION → BEHAVIORAL UPDATE`

Within this specification, experience rules are tracked through:

`R0 Hypothesis → R1 Candidate Experience → R2 Production Rule`

FTD v0.1 is an experimental specification derived from real operational failures.

We make no claim that every underlying idea is unprecedented.

Instead, we intend to document clearly:

- what we define
- what we observe
- what humans correct
- what reality validates
- what remains uncertain
- and how the specification changes over time

---

## Origin

This project began in **China in 2026**.

FTD emerged while Zhang Kang (康哥) and A-Xu (阿序) were working through real business, content-production, and human-AI collaboration failures.

Again and again, the same question appeared:

> **How can a human-AI system avoid paying for the same mistake twice?**

FTD did not begin as a claim of theoretical novelty.

It began as an operational need.

---

## Status

**Kang & A-Xu FTD Specification v0.1**

**Status: Experimental**

FTD is not presented as an established industry standard.

It is not a finished theory.

It is a working specification being tested against real failures.

Future cases may:

- support parts of the specification
- modify parts of it
- reject parts of it
- or produce entirely new rules

FTD itself should be subject to the same principle.

If reality shows that part of FTD v0.1 is wrong, that failure should be recorded, corrected, validated, and used to improve the specification.

> **FTD should be able to learn from its own failures.**

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
