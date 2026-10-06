# Lesson

**Version:** 1.0
**Status:** Contract

---

## 1. Purpose

A Lesson is a self-contained unit of learning material derived from the approved Curriculum Contract.

A lesson exists to help the learner achieve one or more specific approved learning objectives.

Lessons are the primary authoritative learning material presented by the Teacher.

---

## 2. Core Principle

A lesson answers:

> **What does the learner need to understand or be able to do here, and how can that be taught clearly?**

A lesson is not a curriculum.

It must serve the curriculum rather than redefine it.

---

## 3. Lesson Authority

A published lesson is considered stable learning material.

AI must not silently modify a published lesson.

Improvements, corrections, or rewrites require an explicit revision process.

---

## 4. Curriculum Traceability

Every lesson must be traceable to the Curriculum Contract.

A lesson must identify:

* curriculum version;
* module;
* learning objective(s);
* relevant concepts;
* prerequisites.

Example:

```markdown
## Curriculum Alignment

**Curriculum Version:** 1.0

**Module:** Module 3 — Routing

**Learning Objectives:**

- Explain how routers determine where packets should be forwarded.
- Configure basic static routing.

**Prerequisites:**

- IP addressing
- Subnetting
```

A lesson should not exist without a meaningful relationship to the approved curriculum.

---

## 5. Required Lesson Structure

A lesson should normally contain:

```markdown
# Lesson [Number] — [Title]

## Curriculum Alignment

[Traceability information]

## Purpose

[Why this lesson exists]

## Learning Objectives

By the end of this lesson, the learner should be able to:

- [Objective]
- [Objective]

## Prerequisites

- [Prerequisite]

## Concepts

### [Concept]

[Explanation]

## Mental Model

[The simplest useful model for understanding the subject]

## Detailed Explanation

[Detailed instructional content]

## Examples

[Relevant examples]

## Practical Application

[Exercises, experiments, demonstrations, or implementation]

## Common Misconceptions

[Important misconceptions and corrections]

## Summary

[Key ideas]

## Self-Check

[Questions or tasks the learner can use to verify understanding]

## Further Exploration

[Optional supplementary material]

## References

[Relevant references]
```

Not every lesson requires every section.

Sections should exist when they meaningfully support learning.

---

## 6. Learning Objectives

Lesson objectives should be derived from the Curriculum Contract.

Objectives should describe observable understanding or capability.

Prefer:

> Explain why a router selects one route over another.

over:

> Understand routing.

Where practical, objectives should use meaningful action verbs such as:

* explain;
* describe;
* distinguish;
* analyze;
* configure;
* implement;
* troubleshoot;
* design;
* evaluate;
* demonstrate.

---

## 7. Scope

A lesson should have a clear scope.

It should not attempt to teach an entire module unless the module genuinely represents one coherent learning unit.

Avoid:

* unnecessary tangents;
* unrelated domain knowledge;
* excessive historical detail;
* advanced material that belongs later;
* hidden prerequisites.

If additional information is useful but outside the lesson's intended scope, place it in supplementary material or further exploration.

---

## 8. Prerequisites

Prerequisites must be explicit when they materially affect comprehension.

A lesson should not assume knowledge that the learner has no reasonable way to possess.

If an important prerequisite is missing from the Curriculum Contract, the Lesson Author must not silently add it as a curriculum requirement.

Instead, the issue should be surfaced.

---

## 9. Teaching Quality

Lessons should prioritize:

### Clarity

Explain concepts in understandable language.

### Accuracy

Technical claims should be correct and appropriately qualified.

### Depth

Provide enough detail to satisfy the lesson's learning objectives.

### Coherence

Concepts should build on one another logically.

### Relevance

Examples and explanations should support the learning objectives.

### Transfer

Where appropriate, help the learner apply the concept beyond the immediate example.

---

## 10. Mental Models

Where useful, lessons should provide a conceptual mental model.

A mental model should help the learner understand:

* what is happening;
* why it happens;
* how the pieces relate;
* how the concept can be reasoned about.

Mental models should simplify without becoming misleading.

---

## 11. Examples

Examples should reinforce the concepts being taught.

Prefer examples that:

* expose important relationships;
* illustrate realistic situations;
* demonstrate cause and effect;
* help distinguish similar concepts.

Examples should not introduce major concepts that the lesson does not explain unless they are explicitly identified as prerequisites or supplementary material.

---

## 12. Practical Application

When appropriate, lessons should include practical application.

Possible forms include:

* exercises;
* experiments;
* coding tasks;
* configuration tasks;
* troubleshooting scenarios;
* calculations;
* design exercises;
* simulations.

Practical work should have a clear connection to the learning objectives.

---

## 13. Common Misconceptions

Where useful, lessons should explicitly address common misunderstandings.

A misconception section should focus on errors that are:

* common;
* consequential;
* difficult to discover independently;
* likely to interfere with later learning.

Do not create artificial misconceptions merely to fill the section.

---

## 14. Self-Check

Lessons should provide a lightweight way for the learner to verify understanding.

Examples:

* questions;
* explanations in the learner's own words;
* small exercises;
* prediction tasks;
* debugging tasks;
* practical demonstrations.

A self-check is not necessarily a formal assessment.

Formal assessment is handled by the Assessment component.

---

## 15. References

References should be included when useful.

For technical or factual material, references should preferably come from authoritative sources.

The Lesson Author must not fabricate references.

When information is uncertain, disputed, or version-dependent, the lesson should say so.

---

## 16. Immutability

Once a lesson is published, it should be treated as immutable by default.

The following actions must not happen silently:

* rewriting;
* adding sections;
* removing content;
* changing examples;
* changing technical claims;
* changing objectives.

A revision requires an explicit request or an approved change process.

---

## 17. Lesson Revision

A lesson revision should identify:

```markdown
## Revision

**Previous Version:** [Version]

**New Version:** [Version]

**Reason:**

[Why the lesson is being revised]

**Changes:**

- [Change]
- [Change]

**Curriculum Impact:**

[None | Describe impact]

**Approved By:** [Learner / authorized process]
```

If a lesson revision requires a curriculum change, the Curriculum Contract must be revised separately.

A lesson must never use its own revision as a mechanism for silently changing the curriculum.

---

## 18. Curriculum Changes Discovered During Authoring

The Lesson Author may discover that:

* a prerequisite is missing;
* an objective is unclear;
* a module is too broad;
* the curriculum contains an inconsistency;
* an important concept is absent.

The Lesson Author must not silently redesign the curriculum.

Instead, it should report the issue.

Possible outcomes include:

* lesson-level clarification;
* supplementary material;
* curriculum change proposal.

---

## 19. Published Status

A lesson may have:

```text
DRAFT
REVIEW
PUBLISHED
SUPERSEDED
```

### DRAFT

The lesson is being generated or edited.

### REVIEW

The lesson is undergoing explicit review.

### PUBLISHED

The lesson is approved learning material and should be treated as stable.

### SUPERSEDED

A newer approved version replaces this lesson.

Historical versions should remain recoverable when practical.

---

## 20. Lesson Numbering

Lesson numbering should reflect curriculum structure but should not create unnecessary coupling.

A lesson may use identifiers such as:

```text
M01-L01
M01-L02
M02-L01
```

The identifier should remain stable where practical.

If lessons are reordered, avoid unnecessarily changing identifiers unless the meaning of the lesson fundamentally changes.

---

## 21. Relationship to the Teacher

The Teacher uses published lessons as authoritative instructional material.

The Teacher may:

* explain differently;
* provide additional examples;
* adjust pacing;
* ask questions;
* provide remediation;
* provide supplementary material.

The Teacher must not silently rewrite the lesson or curriculum.

---

## 22. Relationship to Assessment

Assessment may evaluate the learning objectives represented by a lesson.

However, the existence of an assessment question does not automatically justify adding new lesson content.

If assessment reveals a problem with the lesson, the issue should be surfaced for review.

---

## 23. Quality Test

A lesson is ready for publication when:

1. Its curriculum alignment is clear.
2. Its objectives are explicit.
3. Its prerequisites are appropriate.
4. Its content supports the objectives.
5. Its explanations are accurate.
6. Its examples are relevant.
7. Its practical work supports learning where appropriate.
8. Important misconceptions are addressed where useful.
9. The learner has a way to self-check understanding.
10. The lesson does not silently expand or modify the curriculum.

---

## 24. Core Principle

> **The curriculum defines what must be learned.
> The lesson defines how a specific part of it is explained and practiced.
> The lesson may evolve when explicitly revised, but it may never silently redefine the curriculum.**

