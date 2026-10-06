# V1 Contract

## Purpose

This document defines the authoritative boundaries of **Version 1 (V1)** of the learning framework.

It converts the conceptual architecture described in `MASTER.md` into a sufficiently explicit contract that the framework can later be validated programmatically and semantically.

V1 is considered complete only when:

1. all required V1 artifacts exist
2. their responsibilities are defined
3. their relationships are defined
4. their authority boundaries are respected
5. their lifecycle rules are consistent
6. their invariants are satisfied
7. the complete system can be exercised through a real learning scenario

This document does not replace the individual artifact contracts.

Instead:

> `MASTER.md` defines the architecture.
> This document defines what constitutes V1.
> Individual contracts define how each component behaves.

---

# V1 Scope

V1 defines a reusable framework for:

```text
Learning Goal
    ↓
Curriculum Design
    ↓
Human Curriculum Approval
    ↓
Lesson Generation
    ↓
Teaching
    ↓
Assessment
    ↓
Progress
    ↓
Revision
```

V1 must support this lifecycle without requiring subject-specific framework logic.

The first real subject used to validate V1 may be domain-specific, but the framework itself must remain subject-agnostic.

---

# V1 Components

V1 consists of the following conceptual components:

```text
Learning Specification
Curriculum Architect
Domain Expert
Curriculum Reviewer
Human Approval
Curriculum Contract
Lesson Author
Published Lessons
Teacher
Assessment
Progress
```

These components are intentionally limited.

V1 does not introduce additional specialized agents unless a concrete requirement demonstrates that an existing role cannot reasonably perform the required responsibility.

---

# V1 Artifacts

The following artifacts constitute the V1 document set.

| Artifact               | Path                                          | Purpose                                            |
| ---------------------- | --------------------------------------------- | -------------------------------------------------- |
| Architecture           | `MASTER.md`                                   | Defines the overall framework architecture         |
| Global AI Rules        | `AI_RULES.md`                                 | Defines cross-framework behavioral rules           |
| Learning Specification | `framework/specification/SPECIFICATION.md`    | Defines the learner's desired outcome              |
| Curriculum Proposal    | `framework/curriculum/CURRICULUM_PROPOSAL.md` | Defines the Architect's proposed curriculum        |
| Expert Critique        | `framework/curriculum/EXPERT_CRITIQUE.md`     | Defines adversarial domain review                  |
| Curriculum Review      | `framework/curriculum/CURRICULUM_REVIEW.md`   | Defines the reconciled curriculum recommendation   |
| Curriculum Contract    | `framework/curriculum/CURRICULUM_CONTRACT.md` | Defines the approved curriculum                    |
| Lesson                 | `framework/lessons/LESSON.md`                 | Defines the structure of durable learning material |
| Lesson Author          | `framework/lessons/LESSON_AUTHOR.md`          | Defines how lessons are produced                   |
| Teacher                | `framework/teacher/TEACHER.md`                | Defines learner-facing teaching behavior           |
| Assessment             | `framework/assessment/ASSESSMENT.md`          | Defines evidence of learning                       |
| Workflow               | `framework/WORKFLOW.md`                       | Defines how the components operate together        |
| V1 Contract            | `framework/validation/V1_CONTRACT.md`         | Defines the V1 boundary and invariants             |

Every artifact listed above is part of V1.

---

# V1 Architecture

The authoritative V1 flow is:

```text
Learner
   ↓
Learning Specification
   ↓
Curriculum Architect
   ↓
Curriculum Proposal
   ↓
Domain Expert
   ↓
Expert Critique
   ↓
Curriculum Reviewer
   ↓
Curriculum Review
   ↓
Human Approval
   ↓
Curriculum Contract
   ↓
Lesson Author
   ↓
Lessons
   ↓
Teacher
   ↓
Assessment
   ↓
Progress
```

Feedback may return to an earlier stage when the type of problem requires it.

---

# Component Responsibilities

## Learning Specification

Defines:

* learner goal
* motivation
* desired depth
* relevant prior knowledge
* practical goals
* theoretical goals
* constraints
* exclusions
* other learner-specific requirements

It represents learner intent.

It does not design the curriculum.

---

## Curriculum Architect

Transforms the Learning Specification into a proposed curriculum.

Responsible for:

* scope
* outcomes
* modules
* dependencies
* progression
* practical application
* assessment strategy
* estimated complexity

Does not approve the curriculum.

---

## Domain Expert

Provides adversarial subject-matter review.

Responsible for identifying:

* technical problems
* missing prerequisites
* sequencing problems
* important omissions
* false completeness
* inappropriate scope
* outdated assumptions
* unnecessary complexity

Does not approve or redesign the curriculum.

---

## Curriculum Reviewer

Synthesizes:

* learner intent
* curriculum proposal
* domain critique

Produces a coherent recommendation for the learner.

Does not approve the curriculum.

---

## Human Approval

The learner has final authority over the curriculum.

Human approval is the transition from:

```text
Recommendation
```

to:

```text
Approved Curriculum Contract
```

AI cannot perform this transition on behalf of the learner.

---

## Curriculum Contract

Defines the authoritative approved curriculum.

It controls:

* required scope
* learning outcomes
* modules
* dependencies
* progression
* practical capabilities
* exclusions
* assessment expectations

All downstream components operate within its boundaries.

---

## Lesson Author

Transforms curriculum requirements into durable lessons.

Responsible for:

* lesson structure
* explanation
* examples
* practical application
* continuity
* prerequisite handling
* curriculum traceability

Does not redefine curriculum.

---

## Teacher

Provides adaptive learner-facing instruction.

Responsible for:

* explanation
* clarification
* adaptation
* practice
* feedback
* remediation
* supplementary teaching

Does not redefine curriculum.

---

## Assessment

Produces evidence about learner achievement.

Responsible for:

* evaluating curriculum objectives
* collecting evidence
* providing feedback
* identifying weaknesses
* supporting progress decisions

Does not define curriculum.

---

## Progress

Represents the learner's demonstrated state relative to curriculum objectives.

Progress is evidence-based.

Progress does not change curriculum scope.

---

# Authority Hierarchy

V1 uses the following authority hierarchy:

```text
Human / Learner
       ↓
Learning Specification
       ↓
Approved Curriculum Contract
       ↓
Published Lessons
       ↓
Teaching / Assessment
```

More precisely:

### Human

Final authority over learner goals and curriculum approval.

### Learning Specification

Defines intended learner outcome.

### Curriculum Contract

Defines approved learning scope.

### Published Lessons

Implement curriculum requirements.

### Teacher

Adapts how the material is taught.

### Assessment

Determines evidence of achievement.

No downstream artifact may override an upstream authority without an explicit revision process.

---

# The Curriculum Contract Boundary

The Curriculum Contract is the central V1 boundary.

Before approval:

```text
AI may propose
AI may critique
AI may synthesize
Human decides
```

After approval:

```text
AI may teach
AI may generate lessons
AI may assess
AI may identify problems
AI may propose changes
Human approves curriculum changes
```

AI must not silently convert observations into curriculum changes.

---

# Artifact States

V1 recognizes the following important lifecycle states.

## Curriculum Proposal

```text
PROPOSED
UNDER_REVIEW
REVISION_REQUIRED
APPROVED
REJECTED
SUPERSEDED
```

`APPROVED` may only be assigned through explicit human approval.

---

## Expert Critique

```text
DRAFT
COMPLETE
SUPERSEDED
```

Expert critique has no approval state.

---

## Curriculum Review

```text
READY_FOR_APPROVAL
REQUIRES_LEARNER_DECISION
REQUIRES_REVISION
INSUFFICIENT_INFORMATION
```

The Reviewer cannot mark the curriculum as approved.

---

## Curriculum Contract

Curriculum Contracts are versioned.

Example:

```text
v1.0
v1.1
v2.0
```

A new approved contract represents an explicit curriculum revision.

---

## Lesson

```text
DRAFT
REVIEW
PUBLISHED
SUPERSEDED
```

Published lessons are stable learning artifacts.

---

# Versioning

V1 uses explicit versions for artifacts where historical identity matters.

At minimum:

* Curriculum Contracts must be versioned.
* Published lessons must identify the Curriculum Contract version they implement.
* Material revisions must preserve sufficient historical information to determine what changed.

V1 does not require a universal versioning algorithm for every document.

---

# Required Traceability

Every published lesson must be traceable to:

```text
Curriculum Contract version
        ↓
Module
        ↓
Objective(s)
        ↓
Concepts
```

Every meaningful assessment must be traceable to:

```text
Curriculum Contract
        ↓
Objective(s)
        ↓
Evidence
```

Every learner progress state must be traceable to evidence where appropriate.

Traceability is required so that curriculum changes can be analyzed for downstream impact.

---

# Core Invariants

The following invariants define fundamental V1 behavior.

## INV-001 — Human Curriculum Authority

Only explicit human approval may create an approved Curriculum Contract.

No AI role may approve a curriculum on behalf of the learner.

---

## INV-002 — Contract Authority

The current Curriculum Contract is authoritative for approved curriculum scope.

Downstream components must operate within it.

---

## INV-003 — No Silent Curriculum Mutation

No AI component may silently add, remove, or modify curriculum requirements.

Curriculum changes require the defined revision process.

---

## INV-004 — Lesson Traceability

Every published lesson must identify the Curriculum Contract version it implements.

---

## INV-005 — Assessment Alignment

Meaningful assessment must evaluate one or more approved curriculum objectives.

---

## INV-006 — No Hidden Curriculum

Supplementary teaching must not silently become required curriculum.

---

## INV-007 — Role Separation

Each component must operate within its defined responsibility.

A component must not silently assume another component's authority.

---

## INV-008 — Published Lesson Stability

A published lesson must not be silently modified.

Changes require an explicit revision.

---

## INV-009 — Curriculum Revision Traceability

Changes to an approved curriculum must produce a new identifiable Curriculum Contract version.

---

## INV-010 — Historical Recoverability

Important previous curriculum and learning-material states must remain recoverable.

The framework must not destroy historical decisions merely because a newer version exists.

---

## INV-011 — Subject Agnosticism

V1 framework logic must not depend on a specific academic or professional domain.

Subject-specific knowledge belongs in the subject materials, expert reasoning, lessons, or curriculum artifacts.

---

## INV-012 — Explicit Uncertainty

When a component cannot confidently determine the correct action, it must surface uncertainty rather than fabricate certainty.

---

## INV-013 — No Unauthorized Scope Expansion

Interesting, useful, or commonly taught information does not automatically become curriculum content.

---

## INV-014 — Assessment Does Not Define Curriculum

Assessment may reveal problems with curriculum design, but cannot silently redefine curriculum requirements.

---

## INV-015 — Teaching Does Not Define Curriculum

The Teacher may adapt explanations and provide supplementary material, but cannot redefine required learning outcomes.

---

## INV-016 — Lesson Author Does Not Design Curriculum

The Lesson Author may identify curriculum problems but must not silently solve them by changing curriculum scope.

---

## INV-017 — Expert Does Not Approve

The Domain Expert provides technical critique.

Technical correctness does not give the Expert authority to approve the learner's curriculum.

---

## INV-018 — Reviewer Does Not Approve

The Curriculum Reviewer produces a recommendation.

The recommendation becomes authoritative only after explicit human approval.

---

## INV-019 — Learner Intent Matters

Curriculum decisions must remain grounded in the Learning Specification.

The system must not optimize for maximum subject coverage when that conflicts with the learner's actual goal.

---

## INV-020 — No Unnecessary Agent Proliferation

V1 must not introduce additional specialized agents unless an actual recurring requirement demonstrates that an existing role cannot reasonably fulfill the responsibility.

---

# Valid Transitions

V1 defines these primary transitions:

```text
Learning Specification
        ↓
Curriculum Proposal

Curriculum Proposal
        ↓
Expert Critique

Curriculum Proposal + Expert Critique
        ↓
Curriculum Review

Curriculum Review
        ↓
Human Approval

Human Approval
        ↓
Curriculum Contract

Curriculum Contract
        ↓
Lesson Author

Lesson Author
        ↓
Lesson

Published Lesson
        ↓
Teacher

Published Lesson + Curriculum Objective
        ↓
Assessment

Assessment
        ↓
Progress
```

These are conceptual transitions.

Implementation may combine or automate operations without changing their semantic meaning.

---

# Invalid Transitions

The following are invalid in V1.

### Expert → Approved Curriculum

The Expert cannot approve.

### Reviewer → Approved Curriculum

The Reviewer cannot approve.

### Teacher → Curriculum Contract

The Teacher cannot directly modify curriculum.

### Assessment → Curriculum Contract

Assessment cannot directly modify curriculum.

### Lesson Author → Curriculum Contract

Lesson authoring cannot silently modify curriculum.

### Published Lesson → Curriculum Change

A lesson problem does not automatically imply a curriculum change.

---

# Revision Transitions

## Lesson Revision

```text
Published Lesson
      ↓
Problem
      ↓
Lesson Revision
      ↓
New Lesson Version
```

The Curriculum Contract remains unchanged unless the problem is actually curricular.

---

## Curriculum Revision

```text
Current Curriculum Contract
      ↓
Change Proposal
      ↓
Impact Analysis
      ↓
Expert Review when necessary
      ↓
Curriculum Review
      ↓
Human Approval
      ↓
New Curriculum Contract
```

---

## Goal Revision

```tex
```

