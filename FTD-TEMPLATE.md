# FTD Record Template

## Kang & A-Xu FTD Specification

Use this template to create a new Failure Training Data record.

An FTD record should preserve the full path from failure to future behavioral change:

`FAILURE → HUMAN CORRECTION → VALIDATION → BEHAVIORAL UPDATE`

A single failure begins as:

`R0 — Hypothesis`

Do not promote a lesson to R1 or R2 without real validation.

---

## 1. Identity

```text
ftd_id:
project:
task:
created_at:
owner:
status:
```

---

## 2. Original Attempt

### Input

What information, instructions, assets, context, or constraints were provided?

```text
input:
```

### Expected Result

What was supposed to happen?

```text
expected_result:
```

### Actual Output

What actually happened?

```text
actual_output:
```

---

## 3. Human Judgment

### Human Rejection Reason

What exactly did the human reject?

Why was the result unacceptable, incomplete, inefficient, unsafe, off-strategy, or otherwise unsuitable?

```text
human_rejection_reason:
```

Avoid vague judgments such as:

```text
bad
wrong
not good enough
```

Record the real reason whenever possible.

### Human Decision

What did the human decide to do next?

```text
human_decision:
```

Human correction does not automatically prove the human is correct.

It creates a hypothesis to be tested.

---

## 4. Failure Diagnosis

### Observed Failure

What failure can actually be observed?

```text
observed_failure:
```

### Root-Cause Hypothesis

Why do we currently believe the failure happened?

```text
root_cause_hypothesis:
```

Keep the hypothesis separate from any later validated cause.

---

## 5. Correction

### Correction Action

What was changed?

```text
correction_action:
```

### Corrected Output

What did the corrected attempt produce?

```text
corrected_output:
```

---

## 6. Validation

### Validation Method

How was the correction tested against reality?

```text
validation_method:
```

### Validation Result

What did reality show?

```text
validation_result:
```

### Validation Count

How many meaningful real-world validations have occurred?

```text
validation_count:
```

### Evidence

What evidence supports or contradicts the lesson?

```text
evidence:
```

Contradictory evidence must also be retained.

---

## 7. Scope

### Applies To

Where does this lesson appear to apply?

```text
applies_to:
```

### Does Not Apply To

Where should this lesson not be assumed to apply?

```text
does_not_apply_to:
```

A useful rule without a scope can become a harmful rule.

---

## 8. Experience Rule Status

Choose one:

```text
R0 — Hypothesis
R1 — Candidate Experience
R2 — Production Rule
```

Current status:

```text
rule_status:
```

### Promotion Rationale

Why does the current evidence justify this rule status?

```text
promotion_rationale:
```

Do not promote a rule only because it sounds reasonable.

---

## 9. Behavioral Update

### Future Behavior Change

What should humans, AI agents, prompts, workflows, routing rules, quality gates, or automations do differently next time?

```text
future_behavior_change:
```

### Affected Roles or Agents

Who or what must inherit this change?

```text
agents_or_roles_affected:
```

If future behavior does not change, organizational learning has not yet occurred.

---

## 10. Evidence Links

Record links or references to the relevant artifacts.

```text
original_artifact:
corrected_artifact:
human_feedback:
metrics_or_real_world_result:
related_ftd_records:
```

---

## 11. Contradictory Evidence

Has later evidence challenged this lesson?

```text
contradictory_evidence:
```

If yes, record whether the rule should be:

```text
reviewed
downgraded
modified
retired
```

An R2 rule is not permanent truth.

> **Reality has final authority.**

---

## 12. Final FTD Test

Before treating this record as reusable organizational experience, ask:

1. Is the failure clearly described?
2. Is the human correction clearly described?
3. Has the correction faced reality?
4. Is observation separated from hypothesis?
5. Is the rule status supported by evidence?
6. Is the scope defined?
7. Is contradictory evidence preserved?
8. Will future behavior change because this failure happened?

Final question:

> **If another human or AI agent reads this record tomorrow, will it behave differently because this failure happened?**

If the answer is no, the FTD record is incomplete.

---

## Project Identity

**Kang & A-Xu**

A project initiated by **Zhang Kang (康哥)**, developed with **A-Xu (阿序)**, an AI collaborator.

Copyright © 2026 Zhang Kang
