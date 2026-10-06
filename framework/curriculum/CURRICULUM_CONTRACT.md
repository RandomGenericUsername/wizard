# Curriculum Contract

**Version:** 1.0
**Status:** Contract

---

## 1. Purpose

The Curriculum Contract is the authoritative definition of what the learner has agreed to learn.

It is created when the learner explicitly approves a Curriculum Review.

It establishes the boundary between:

* AI-generated curriculum proposals;
* human-approved curriculum;
* future learning material.

Once approved, the Curriculum Contract becomes the authoritative curriculum for the learning program.

---

## 2. Core Principle

Before approval:

> The curriculum is a proposal.

After approval:

> The curriculum is a contract.

AI may propose changes to the contract.

AI may not silently change it.

---

## 3. Creation

The Curriculum Contract is created from an approved Curriculum Review.

The learner must explicitly approve the curriculum.

Examples of valid approval:

* "Approve."
* "This curriculum looks good."
* "Let's use this curriculum."
* Explicit approval through a future framework interface.

Silence, continued conversation, or generation of lessons does not constitute approval.

---

## 4. Authority

The Curriculum Contract is authoritative for:

* learning scope;
* required modules;
* required learning outcomes;
* progression;
* major prerequisites;
* required practical capabilities;
* explicit exclusions;
* approved constraints;
* curriculum-level assessment expectations.

Other AI components must operate within these boundaries.

---

## 5. Required Structure

A Curriculum Contract should contain:

```markdown id="x2q6hd"
# Curriculum Contract

**Status:** APPROVED

## Curriculum Goal

[Approved goal]

## Scope

### Required

- [Required area]

### Supporting

- [Supporting area]

### Optional

- [Optional area]

### Excluded

- [Excluded area]

## Learning Outcomes

By completing this curriculum, the learner should be able to:

- [Outcome]
- [Outcome]

## Curriculum Structure

### Module 1 — [Name]

**Purpose**

[Purpose]

**Learning Objectives**

- [Objective]

**Major Concepts**

- [Concept]

**Prerequisites**

- [Prerequisite]

**Practical Capabilities**

- [Capability]

---

### Module 2 — [Name]

...

## Dependencies

[Approved dependencies]

## Progression

[Approved progression]

## Practical Application

[Approved practical work]

## Assessment Strategy

[Approved assessment approach]

## Learner Decisions

[Important decisions made by the learner]

## Explicit Exclusions

[Topics explicitly excluded]

## Approved Assumptions

[Important assumptions accepted as part of the curriculum]

## Approval

**Approved By:** Learner

**Approval Date:** [Date]

**Source Review:** [Reference to Curriculum Review]

**Curriculum Version:** 1.0
```

---

## 6. Required Distinctions

The contract must clearly distinguish:

### Required

The learner is expected to learn this.

### Supporting

This supports required learning but may not represent a major independent learning objective.

### Optional

Useful material that does not form part of the required curriculum.

### Excluded

Material intentionally outside the curriculum.

These distinctions prevent supplementary material from silently becoming required curriculum.

---

## 7. Immutability

The Curriculum Contract is **immutable by default**.

"Immutable" means that AI components cannot modify it as part of normal operation.

This includes the:

* Teacher;
* Lesson Author;
* Assessment system;
* Domain Expert;
* other future AI components.

A change requires an explicit curriculum revision process.

---

## 8. Curriculum Revision

A curriculum revision follows this general process:

```text id="p8jz7n"
Existing Curriculum Contract
          ↓
Change Proposal
          ↓
Impact Analysis
          ↓
Curriculum Revision
          ↓
Expert Review (when necessary)
          ↓
Curriculum Review
          ↓
Human Approval
          ↓
New Curriculum Contract Version
```

The original approved version should remain recoverable.

---

## 9. Change Proposal

A change proposal should explain:

```markdown id="8nq3xk"
# Curriculum Change Proposal

## Requested Change

[What should change]

## Reason

[Why the change is being proposed]

## Affected Areas

- [Module]
- [Outcome]
- [Dependency]

## Consequences

[What changes if approved]

## Alternatives

[Alternative approaches, if relevant]

## Recommendation

[Recommended action]
```

The change proposal is not itself an approved change.

---

## 10. Versioning

Curriculum Contracts must be versioned.

Use semantic-style versioning where practical:

```text
MAJOR.MINOR
```

Examples:

```text
1.0
1.1
1.2
2.0
```

### Minor Version

Use for changes that do not fundamentally redefine the curriculum.

Examples:

* clarification of an outcome;
* small sequencing adjustment;
* refinement of supporting material;
* correction that does not change the fundamental scope.

### Major Version

Use when the learner's approved learning contract materially changes.

Examples:

* major scope expansion;
* major scope reduction;
* substantial restructuring;
* new primary learning goals;
* removal of major required areas.

The learner must explicitly approve major revisions.

---

## 11. Historical Versions

Previous approved curriculum versions should remain identifiable.

For example:

```text
Curriculum Contract v1.0
        ↓
Curriculum Contract v1.1
        ↓
Curriculum Contract v2.0
```

The current version is authoritative.

Historical versions provide context for how the learning program evolved.

---

## 12. AI Behavior

Every AI component must treat the Curriculum Contract as authoritative.

When operating under an approved contract, AI should:

1. read the current contract;
2. respect required and excluded areas;
3. respect approved progression;
4. avoid silently changing requirements;
5. distinguish optional material from required material;
6. surface conflicts rather than silently resolving them;
7. propose curriculum changes when necessary.

---

## 13. Discovering a Curriculum Gap

If an AI component discovers something that appears to be missing:

It must **not** automatically add it to the curriculum.

Instead:

```text id="9z3h1v"
Discover Gap
     ↓
Explain Why It Matters
     ↓
Determine Whether It Is:
  - Supplementary
  - Curriculum Issue
  - Prerequisite Issue
     ↓
If Curriculum Change Is Needed
     ↓
Create Change Proposal
```

This applies even when the AI believes the missing topic is important.

---

## 14. Curriculum vs Supplementary Material

The Curriculum Contract defines the authoritative learning requirements.

The Teacher and other components may provide supplementary material without modifying the contract.

For example:

**Contract:**

> Learner must understand TCP connection establishment.

**Teacher supplementary material:**

> Here is an optional historical explanation of how early TCP implementations handled connection setup.

The supplementary material does not become a new curriculum requirement.

---

## 15. Relationship to Lessons

Lessons must be derived from the Curriculum Contract.

A lesson should be traceable to:

* a module;
* one or more learning objectives;
* relevant concepts;
* the approved progression.

A Lesson Author must not create required lessons for curriculum objectives that do not exist in the contract without first proposing a curriculum change.

---

## 16. Relationship to Assessment

Assessment should evaluate the approved curriculum.

The Assessment system may identify:

* missing knowledge;
* weak understanding;
* inadequate practical capability;
* potential curriculum problems.

However, assessment results do not automatically modify the Curriculum Contract.

If assessment reveals a curriculum problem, it should produce a recommendation for review.

---

## 17. Relationship to Teacher

The Teacher operates within the Curriculum Contract.

The Teacher may adapt:

* explanation;
* pacing;
* examples;
* exercises;
* supplementary material;
* remediation.

The Teacher must not silently change:

* required scope;
* learning outcomes;
* curriculum progression;
* explicit exclusions.

---

## 18. Approval Boundary

The following distinction must always remain clear:

```text
AI proposes
     ↓
AI critiques
     ↓
AI reviews
     ↓
Human approves
     ↓
Curriculum becomes authoritative
```

Human approval is the transition from proposal to contract.

---

## 19. Quality Test

A valid Curriculum Contract should allow the system to answer unambiguously:

1. What is the learner committed to learning?
2. What is required?
3. What is optional?
4. What is excluded?
5. What outcomes are expected?
6. What progression was approved?
7. What major prerequisites were approved?
8. What practical capabilities are expected?
9. What decisions did the learner explicitly make?
10. What version is currently authoritative?

If these questions cannot be answered, the Curriculum Contract is insufficiently defined.

---

## 20. Core Principle

> **The AI may recommend the road.
> The learner chooses the road.
> Once chosen, the road becomes the contract.
> AI may suggest changing it, but AI cannot silently redraw it.**

