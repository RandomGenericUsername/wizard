# Curriculum Proposal

**Version:** 1.0
**Status:** Contract

---

## 1. Purpose

The Curriculum Proposal is the structured output of the Curriculum Architect.

It transforms a learner's Learning Specification into a proposed learning path.

It answers:

> **Given what the learner wants to achieve, what should they learn, in what order, and to what depth?**

The proposal is **not yet authoritative**.

It must be reviewed by the Domain Expert, evaluated by the Curriculum Reviewer, and ultimately approved by the learner before becoming the Curriculum Contract.

---

## 2. Core Principle

The Curriculum Architect is responsible for designing the learning path.

The Architect must not simply produce a list of topics.

A curriculum should describe:

* what the learner needs to learn;
* why it matters;
* how concepts depend on each other;
* how knowledge progresses;
* where practical application occurs;
* what depth is appropriate;
* how the curriculum supports the learner's goals.

---

## 3. Required Information

A Curriculum Proposal must contain the following.

### 3.1 Curriculum Goal

A concise description of what the curriculum is designed to accomplish.

It should directly correspond to the learner's primary goal.

---

### 3.2 Scope

Define what the curriculum covers.

The scope should distinguish between:

* core required knowledge;
* supporting knowledge;
* advanced or optional knowledge;
* explicitly excluded areas.

---

### 3.3 Learning Outcomes

Describe what the learner should be able to understand or do after completing the curriculum.

Outcomes should be observable where practical.

Prefer:

> Diagnose common routing failures and explain the underlying cause.

over:

> Understand routing.

---

### 3.4 Curriculum Structure

The curriculum should be divided into meaningful stages, modules, or phases.

Each stage should represent a coherent learning unit rather than an arbitrary collection of topics.

---

### 3.5 Module Definitions

Each module should identify:

* purpose;
* learning objectives;
* major concepts;
* practical capabilities;
* prerequisites;
* relationship to learner goals.

---

### 3.6 Dependencies

The proposal must identify important prerequisite relationships.

For example:

```text
IP addressing
      ↓
Subnetting
      ↓
Routing
      ↓
Routing protocols
```

Dependencies should reflect actual conceptual or practical requirements rather than merely preferred ordering.

---

### 3.7 Progression

Explain how the curriculum progresses from simpler knowledge toward more complex capability.

Progression may involve:

* conceptual complexity;
* practical complexity;
* abstraction;
* system scale;
* independence;
* integration of previously learned concepts.

---

### 3.8 Practical Application

Identify where practical work should reinforce learning.

Examples:

* exercises;
* experiments;
* labs;
* projects;
* troubleshooting scenarios;
* implementation tasks.

Practical activities should support learning objectives rather than exist merely for variety.

---

### 3.9 Assessment Strategy

At the curriculum level, identify how the learner's progress can eventually be demonstrated.

This does not require writing individual assessment questions.

Examples:

* conceptual explanations;
* practical configuration;
* troubleshooting;
* design tasks;
* projects;
* progressively integrated exercises.

---

### 3.10 Estimated Complexity

The proposal should communicate the expected scale of the curriculum.

This may include:

* approximate number of modules;
* relative difficulty;
* major stages;
* expected progression.

Exact lesson counts are not required at this stage.

The Architect should avoid inventing artificial precision.

---

## 4. Recommended Structure

A Curriculum Proposal should normally use this structure:

```markdown
# Curriculum Proposal

## Curriculum Goal

[What this curriculum is intended to achieve]

## Scope

### Core

- [Required area]
- [Required area]

### Supporting

- [Supporting area]

### Advanced / Optional

- [Optional area]

### Excluded

- [Explicitly excluded area]

## Learning Outcomes

By completing this curriculum, the learner should be able to:

- [Outcome]
- [Outcome]
- [Outcome]

## Curriculum Structure

### Module 1 — [Name]

**Purpose**

[Why this module exists]

**Learning Objectives**

- [Objective]
- [Objective]

**Major Concepts**

- [Concept]
- [Concept]

**Practical Capabilities**

- [Capability]

**Prerequisites**

- [Prerequisite]

**Learner Goals Supported**

- [Goal]

---

### Module 2 — [Name]

...

## Dependencies

[Important prerequisite relationships]

## Progression

[Explanation of how complexity increases]

## Practical Application

[Exercises, labs, projects, or other practical work]

## Assessment Strategy

[How learning will eventually be demonstrated]

## Estimated Complexity

[Expected scale and difficulty]

## Architect Notes

[Important design decisions, assumptions, or unresolved questions]
```

---

## 5. Curriculum Design Principles

### 5.1 Start From Outcomes

The Architect should work backward from the learner's desired capabilities.

Do not begin by asking:

> What topics exist in this field?

Begin with:

> What must the learner be capable of doing or understanding?

---

### 5.2 Respect Prerequisites

Important concepts should appear when the learner has sufficient foundation to understand them.

Avoid introducing advanced concepts merely because they are important in the domain.

---

### 5.3 Avoid Topic Dumping

A curriculum is not an encyclopedia index.

Every required topic should have a reason for being included.

The Architect should be able to explain how a major curriculum element contributes to the learner's goals.

---

### 5.4 Avoid False Completeness

The Architect should not claim that the curriculum covers an entire domain unless that claim is justified.

Large domains contain more knowledge than any individual curriculum can reasonably include.

The curriculum should optimize for the learner's goals.

---

### 5.5 Balance Theory and Practice

Where practical application is relevant, concepts should eventually be connected to meaningful application.

The curriculum should not become either:

* pure theoretical study; or
* a sequence of procedures without understanding.

The appropriate balance depends on the Learning Specification.

---

### 5.6 Minimize Unnecessary Complexity

The Architect should not create additional modules, topics, or stages merely to make the curriculum appear comprehensive.

Complexity must serve the learner's goal.

---

## 6. Relationship to Learning Specification

The Curriculum Proposal must be derived from the Learning Specification.

The Architect should explicitly account for:

* primary goal;
* desired depth;
* prior knowledge;
* practical goals;
* theoretical goals;
* constraints;
* exclusions;
* external requirements.

If the Architect believes the specification contains a contradiction or missing requirement that materially affects the curriculum, the issue should be surfaced rather than silently resolved.

---

## 7. Assumptions

The Architect may make reasonable assumptions when necessary.

However:

* assumptions must be identifiable;
* important assumptions should be recorded;
* assumptions that materially affect scope should be surfaced to the learner.

The Architect must not silently turn assumptions into learner requirements.

---

## 8. Domain Knowledge

The Curriculum Architect may use domain knowledge to construct a curriculum.

However, the Architect should not assume that its domain knowledge is sufficient to validate the curriculum.

That is one reason the framework contains a separate **Domain Expert** role.

The Domain Expert exists to challenge the proposal from the perspective of domain correctness and completeness.

---

## 9. What the Curriculum Proposal Must Not Do

The proposal must not:

* become the final approved curriculum without human approval;
* silently override learner constraints;
* silently add excluded material as required;
* define individual lesson content;
* define detailed teaching scripts;
* replace the Domain Expert's adversarial review;
* replace the Curriculum Reviewer's final synthesis;
* silently modify an existing approved curriculum.

---

## 10. Reviewability

The proposal should be easy for another AI component and the learner to inspect.

Major decisions should be explicit.

A reviewer should be able to determine:

* why major modules exist;
* what each module contributes;
* what prerequisites exist;
* how the progression works;
* how the curriculum supports the learner's goals;
* what assumptions were made;
* what remains uncertain.

---

## 11. Status

A Curriculum Proposal can have one of the following statuses:

```text
PROPOSED
UNDER_REVIEW
REVISION_REQUIRED
APPROVED
REJECTED
SUPERSEDED
```

Only `APPROVED` allows the proposal to become the basis of the Curriculum Contract.

An AI component must not assign `APPROVED` status on behalf of the learner.

---

## 12. Revision

A Curriculum Proposal may be revised during the review process.

Revisions should preserve the reasoning behind significant changes.

When practical, changes should make clear:

* what changed;
* why it changed;
* what triggered the change.

The goal is not to create bureaucratic version history for every edit, but to preserve meaningful curriculum decisions.

---

## 13. Relationship to Other Artifacts

The Curriculum Proposal:

**Consumes**

* Learning Specification

**Is evaluated by**

* Domain Expert
* Curriculum Reviewer

**Requires**

* Human Approval

**Produces**

* Approved Curriculum / Curriculum Contract

The proposal does not directly produce lessons.

Lessons are generated only after the curriculum has been approved.

---

## 14. Quality Test

A Curriculum Proposal is ready for review when another competent person or AI can answer:

1. What is this learner trying to achieve?
2. Why is each major stage necessary?
3. What should the learner be able to do after completing it?
4. What prerequisites exist?
5. Why is the progression ordered this way?
6. What is required versus optional?
7. What important assumptions were made?
8. What practical experience will reinforce the concepts?
9. How will learning eventually be demonstrated?
10. What does the curriculum deliberately leave outside its scope?

If these questions cannot be answered, the proposal is not sufficiently defined for adversarial review.

