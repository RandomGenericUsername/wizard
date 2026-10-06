# V1 Contract

## Purpose

This document defines the authoritative boundaries of **Version 1 (V1)** of the learning framework.

It converts the conceptual architecture described in `MASTER.md` into a sufficiently explicit contract that the framework can later be validated programmatically and semantically.

This document defines V1 for the **framework layer**.

It defines how learning systems operate. It does not contain, and must never contain, the knowledge or curriculum of any subject.

Concrete learning programs live in separate **Learning Projects**, as defined in `MASTER.md` section 16.

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
Evidence
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
Evidence
Progress
```

These components are intentionally limited.

Not every component is an agent. `Curriculum Contract` and `Published Lessons` are artifacts. `Evidence` and `Progress` are derived outputs and states rather than autonomous roles.

`Evidence` is the learning evidence produced and recorded by Assessment. It is a derived output, not an agent, and holds no authority of its own.

`Progress` is an evidence-derived state and reporting function. It is not a separate agent and holds no independent authority.

The canonical V1 relationship between these three is:

```text
Assessment → Evidence → Progress
```

Where:

* **Assessment** evaluates and produces evidence.
* **Evidence** is learning evidence.
* **Progress** is learner state derived from that evidence.

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

### Framework Artifacts Are Definitions, Not Instances

Every artifact above is a **framework artifact**: a contract, specification, role definition, or rule.

They define what an artifact of that kind is and what it must contain.

They are not subject knowledge, and they are not instances of themselves.

For example:

```text
Framework Artifact:
framework/curriculum/CURRICULUM_PROPOSAL.md

Project Artifact:
network-infrastructure/curriculum/CURRICULUM_PROPOSAL.md
```

The first defines the Curriculum Proposal artifact contract. The second is an actual Curriculum Proposal for one learner.

The distinction between definition and instance applies to every artifact in the table above.

A Learning Project may instantiate these contracts. V1 defines that relationship only; V1 does not scaffold, generate, or contain any project instance.

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
Evidence
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

## Evidence

Evidence is the learning evidence produced and recorded by Assessment about the learner's achievement.

Evidence is a derived output, not an agent.

Evidence does not make decisions and holds no authority.

Evidence is:

* produced by Assessment
* recorded as historical observation
* interpreted by Progress against the approved Curriculum Contract
* not itself a curriculum requirement
* not itself a mastery decision

The relationship is:

```text
Assessment evaluates → Evidence records → Progress derives
```

Evidence must be sufficient to support a meaningful conclusion about the capability it addresses.

Evidence does not define what the learner must learn. Requirements come from the Curriculum Contract.

Progress may not invent mastery criteria. Where the Curriculum Contract or the applicable assessment criteria define them, Progress applies them to the available evidence.

---

## Progress

Represents the learner's demonstrated state relative to curriculum objectives.

Progress is an evidence-derived state and reporting function.

It is not an autonomous agent, and it does not hold independent authority.

Progress is derived:

```text
Curriculum Contract
        ↓
Objectives
        ↓
Teacher / Lessons
        ↓
Assessment
        ↓
Evidence
        ↓
Progress
```

Assessment owns the evidence.

Progress interprets and reports that evidence against the approved Curriculum Contract.

Progress does not:

* define curriculum;
* define assessment criteria;
* invent mastery criteria;
* create learning requirements;
* approve curriculum;
* replace Assessment;
* replace the Teacher;
* modify lessons;
* alter or discard recorded evidence;
* change curriculum scope.

Progress is evidence-based.

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
Teaching
       ↓
Assessment
       ↓
Evidence
       ↓
Progress
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

### Evidence

Records what Assessment determined.

It is a derived output, not an authority.

### Progress

Reports learner state derived from that evidence.

Progress sits below Assessment and Evidence in the hierarchy. It reports evidence; it does not create it, define it, or turn it into a curriculum requirement.

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

## Progress

```text
NOT_STARTED
INTRODUCED
PRACTICING
DEVELOPING
DEMONSTRATED
MASTERED
```

These are the authoritative V1 progress states.

### NOT_STARTED

No meaningful learning activity or evidence has yet been recorded for the objective.

### INTRODUCED

The learner has been exposed to the objective.

### PRACTICING

The learner is actively practicing the objective but has not yet demonstrated reliable capability.

### DEVELOPING

Evidence shows meaningful progress, but capability is not yet consistently demonstrated.

### DEMONSTRATED

The learner has provided sufficient evidence of the expected capability.

### MASTERED

The learner has demonstrated sustained and reliable capability according to the applicable curriculum and assessment criteria.

Progress states are derived from Assessment evidence.

The existence of a lesson, or the completion of a lesson, must not automatically produce a progress state or a mastery state.

Progress must not invent mastery criteria. Where the Curriculum Contract or the applicable assessment criteria define them, Progress applies them.

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

This applies to repository content as well as to framework logic.

The framework repository must not accumulate subject-specific learning knowledge, and must not contain a concrete Learning Project instance.

Subject knowledge belongs exclusively in Learning Projects.

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
Evidence

Evidence
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
Existing Curriculum Contract
      ↓
Change Proposal
      ↓
Impact Analysis
      ↓
Curriculum Revision
      ↓
Domain Expert Review
      ↓
Curriculum Review
      ↓
Human Approval
      ↓
New Curriculum Contract Version
      ↓
Supersedes the previous Contract version
```

The Curriculum Architect owns the creation of the curriculum revision.

The Reviewer evaluates and synthesizes the revised curriculum.

The Reviewer does not author the Curriculum Architect's proposal, and does not independently decide whether impact analysis is necessary for a curriculum change.

Responsibility during curriculum revision:

```text
Architect  → creates the revision
Expert     → critiques the revision
Reviewer   → evaluates and synthesizes the revision
Human      → approves the revision
```

The new version supersedes the previous version, which remains identifiable as historical context.

---

## Learning Specification Revision

```text
Existing Learning Specification
      ↓
Learning Specification Change
      ↓
Impact Analysis
      ↓
Revised Learning Specification
      ↓
Curriculum Impact Evaluation
      ↓
Curriculum Revision when necessary
      ↓
Human Approval where the curriculum changes
```

### Why this revision is different

Changing the Learning Specification may invalidate or change the intended destination.

It can therefore require substantial curriculum redesign.

Changing the Curriculum Contract requires the curriculum revision process and explicit human approval.

### The Learning Specification is not the Curriculum Contract

The Learning Specification represents learner intent.

It is not an authoritative curriculum artifact and it does not become one.

The Learning Specification is the learner's own statement of intent, so the learner decides changes to it.

There is no separate AI approval system for specifications, and no AI component may revise the learner's stated intent on their behalf.

### Relationship to curriculum approval

The only approval that changes what the learner is required to learn is approval of a Curriculum Contract.

Therefore:

```text
Specification change
        ↓
may or may not affect the curriculum
        ↓
if it affects the curriculum
        ↓
the existing curriculum revision process applies
        ↓
including explicit human approval of the new Contract version
```

A change to the Learning Specification never silently changes the Curriculum Contract.

