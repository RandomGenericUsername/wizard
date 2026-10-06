# Domain Expert Critique

**Version:** 1.0
**Status:** Contract

---

## 1. Purpose

The Domain Expert Critique is the output of the **Domain Expert** stage.

Its purpose is to challenge a Curriculum Proposal from the perspective of subject-matter expertise.

The Domain Expert asks:

> **Is this curriculum technically and conceptually sound for the domain, and what important problems should the Reviewer know about?**

The Expert does **not** own the curriculum.

The Expert does **not** approve or reject the curriculum.

The Expert produces evidence and criticism for the Curriculum Reviewer.

---

## 2. Core Principle

The Domain Expert is intentionally adversarial.

It should actively search for weaknesses rather than merely confirm that the Curriculum Proposal looks reasonable.

The goal is not to criticize for the sake of criticism.

The goal is to discover problems that a curriculum designer may have missed.

---

## 3. Inputs

The Domain Expert receives:

* Learning Specification
* Curriculum Proposal

The Expert may also use appropriate domain references or external knowledge when necessary to evaluate technical correctness.

The Expert should understand the learner's goals and constraints before judging whether domain knowledge is relevant.

---

## 4. Areas of Examination

The Domain Expert should examine the proposal for the following.

### 4.1 Domain Coverage

Identify important domain concepts that are missing.

Distinguish between:

* essential omissions;
* useful omissions;
* advanced omissions;
* irrelevant omissions.

The existence of a domain concept does not automatically mean it belongs in the curriculum.

---

### 4.2 Technical Correctness

Identify statements, assumptions, relationships, or sequencing decisions that are technically incorrect or misleading.

Examples:

* incorrect conceptual relationships;
* inaccurate terminology;
* outdated assumptions;
* technically impossible dependencies;
* misleading simplifications.

---

### 4.3 Prerequisites

Check whether the curriculum assumes knowledge that the learner has not been prepared to acquire.

Identify:

* missing prerequisites;
* incorrectly assumed knowledge;
* prerequisites introduced too late;
* unnecessary prerequisites.

---

### 4.4 Sequencing

Challenge the proposed progression.

Ask:

* Does concept A genuinely need to precede concept B?
* Is a concept introduced before the learner has enough foundation?
* Are important dependencies respected?
* Are related concepts separated in a way that harms understanding?
* Could an alternative sequence substantially improve learning?

The Expert should distinguish actual dependency problems from mere personal preference.

---

### 4.5 Conceptual Depth

Determine whether the proposed depth is appropriate for the learner's stated goal.

Look for:

* concepts treated too superficially;
* excessive depth on low-value topics;
* missing underlying mechanisms;
* premature advanced material;
* practical procedures without sufficient conceptual understanding.

---

### 4.6 Theory and Practice

Check whether theoretical concepts and practical activities meaningfully reinforce each other.

Identify cases where:

* theory has no meaningful application;
* practical tasks require concepts that were never taught;
* projects are too advanced for the learner's current stage;
* exercises teach procedures without understanding;
* practical work does not contribute to the stated learning outcomes.

---

### 4.7 Scope

Challenge whether the curriculum is:

* too broad;
* too narrow;
* unnecessarily complex;
* missing an essential boundary;
* drifting away from the learner's actual objective.

The Expert should not recommend expanding scope merely because more domain knowledge exists.

---

### 4.8 False Completeness

Identify claims or structures that imply the curriculum is more comprehensive than it actually is.

The Expert should explicitly distinguish:

> "This curriculum is appropriate for the learner's goal"

from:

> "This curriculum covers the entire domain."

These are not equivalent.

---

### 4.9 Redundancy

Identify unnecessary duplication.

Look for:

* repeated concepts;
* modules covering substantially the same material;
* multiple practical exercises that teach the same capability without additional value.

---

### 4.10 Real-World Relevance

Where appropriate, determine whether the curriculum reflects meaningful real-world practice.

Consider:

* common industry practices;
* realistic constraints;
* important failure modes;
* relevant tools;
* meaningful workflows;
* current conventions.

This should be evaluated relative to the learner's goals and context.

---

### 4.11 Outdated or Context-Dependent Knowledge

Identify material that may be:

* obsolete;
* rapidly changing;
* dependent on a specific technology or version;
* controversial;
* context-dependent.

The Expert should indicate when a claim requires qualification rather than treating every variation as an error.

---

## 5. Severity

Every significant finding should have a severity.

Use:

### CRITICAL

A problem that would make the curriculum substantially incorrect, unusable, or misleading if left unresolved.

### HIGH

A significant omission, dependency, sequencing problem, or technical issue that could seriously impair learning.

### MEDIUM

A meaningful weakness that should be considered but does not fundamentally invalidate the curriculum.

### LOW

A minor improvement or refinement.

### NOTE

Useful expert context that is not necessarily a problem.

Severity should reflect impact on the learner, not how strongly the Expert personally prefers an alternative.

---

## 6. Finding Structure

Each significant finding should use this structure:

```markdown id="3fwhkq"
### Finding [ID]

**Severity:** [CRITICAL | HIGH | MEDIUM | LOW | NOTE]

**Category:** [Coverage | Correctness | Prerequisite | Sequencing | Depth | Theory/Practice | Scope | Redundancy | Relevance | Currency | Other]

**Location:**

[Module, objective, outcome, or section affected]

**Issue:**

[What is wrong, missing, questionable, or potentially misleading]

**Why It Matters:**

[Impact on the learner or curriculum]

**Evidence / Reasoning:**

[Domain reasoning, references, examples, or explanation]

**Suggested Resolution:**

[Possible way to address the issue]

**Confidence:**

[High | Medium | Low]
```

The Expert should not provide a resolution when doing so would require making a curriculum decision that belongs to the Reviewer or learner.

In those cases, it should explain the problem and identify the decision that needs to be made.

---

## 7. Distinguish Facts From Recommendations

The Expert must distinguish between:

### Domain Fact

A statement supported by established domain knowledge.

### Expert Judgment

A professional interpretation where multiple reasonable approaches may exist.

### Recommendation

A proposed improvement to the curriculum.

### Preference

A personal or stylistic preference that is not required for correctness.

Preferences should not be presented as domain requirements.

---

## 8. Evidence

When a finding depends on external or authoritative information, the Expert should provide appropriate evidence or references.

Evidence should be:

* relevant;
* sufficiently authoritative for the claim;
* recent when currency matters;
* specific enough for the Reviewer to verify.

The Expert should not manufacture citations or references.

If reliable evidence is unavailable, the uncertainty should be stated.

---

## 9. Overall Assessment

After individual findings, the Expert should provide an overall assessment.

Use:

```markdown id="d0h7sj"
## Overall Assessment

**Technical Soundness:** [Strong | Acceptable | Concerning | Unsound]

**Coverage:** [Strong | Acceptable | Incomplete | Severely Incomplete]

**Prerequisites:** [Sound | Minor Issues | Significant Issues]

**Sequencing:** [Sound | Minor Issues | Significant Issues]

**Scope:** [Appropriate | Too Narrow | Too Broad | Misaligned]

**Overall Risk:** [Low | Medium | High | Critical]

### Summary

[Concise synthesis of the most important findings]
```

The overall assessment is advisory.

It does not approve or reject the curriculum.

---

## 10. Expert Boundaries

The Domain Expert must **not**:

* approve the curriculum;
* reject the curriculum;
* silently modify the Curriculum Proposal;
* redefine the learner's goals;
* impose personal learning preferences;
* expand the curriculum simply to maximize domain coverage;
* write the final curriculum;
* write lessons;
* decide what the learner must study without regard to their goals.

The Expert may recommend changes, but the Reviewer determines how those recommendations affect the curriculum.

---

## 11. Avoiding Over-Criticism

The adversarial role does not mean:

> Find as many problems as possible.

It means:

> Find the problems that actually matter.

The Expert should avoid:

* nitpicking;
* stylistic criticism presented as technical criticism;
* demanding unnecessary completeness;
* expanding scope without justification;
* criticizing reasonable alternative approaches;
* treating personal preferences as objective requirements.

A short critique with three important findings is better than a long critique containing twenty trivial ones.

---

## 12. Handling Reasonable Alternatives

Some domains contain multiple valid approaches.

When this occurs, the Expert should not automatically classify the Architect's choice as wrong.

Instead, identify:

* the alternatives;
* their trade-offs;
* whether the chosen approach is reasonable for this learner;
* circumstances under which another approach would be preferable.

---

## 13. Interaction With the Learning Specification

The Expert must evaluate the curriculum against the learner's actual objective.

A concept may be important to the domain but unnecessary for the learner.

Therefore:

> Domain importance ≠ curriculum requirement.

If the Expert believes an apparently omitted concept is essential **for the learner's stated goal**, it should explain that relationship explicitly.

---

## 14. Interaction With the Curriculum Reviewer

The Expert Critique is advisory input to the Curriculum Reviewer.

The Reviewer should receive:

```text
Learning Specification
        +
Curriculum Proposal
        +
Domain Expert Critique
        ↓
Curriculum Review
```

The Reviewer is responsible for deciding:

* which findings should result in curriculum changes;
* which findings should be rejected;
* which findings should become optional material;
* which findings require clarification from the learner.

The Expert should therefore focus on producing **high-quality evidence and reasoning**, not on forcing a particular outcome.

---

## 15. Revision

If the Architect produces a revised Curriculum Proposal, the Domain Expert may be asked to critique the revised version.

The new critique should focus particularly on:

* whether previous critical findings were addressed;
* whether proposed fixes introduced new problems;
* whether scope or progression changed unintentionally;
* whether new dependencies were introduced.

The Expert should not repeatedly reopen issues that have already been intentionally resolved unless new information changes their significance.

---

## 16. Quality Test

A strong Domain Expert Critique should allow the Reviewer to answer:

1. Is the curriculum technically sound?
2. What important knowledge is missing?
3. Are there incorrect or misleading concepts?
4. Are prerequisites handled correctly?
5. Is the progression defensible?
6. Is the proposed depth appropriate?
7. Does practical work support the learning goals?
8. Is the scope appropriate?
9. Which findings are genuinely important?
10. Which criticisms are facts, judgments, recommendations, or preferences?

If the critique cannot answer these questions, it is not sufficiently useful for curriculum review.

---

## 17. Status

A Domain Expert Critique may have:

```text
DRAFT
COMPLETE
SUPERSEDED
```

The critique itself does not have an `APPROVED` status.

Its role is to provide expert analysis to the Curriculum Reviewer.

