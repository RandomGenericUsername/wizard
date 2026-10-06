# Learning Framework Workflow

## Purpose

This document defines the operational lifecycle of the learning framework.

It describes how the framework moves from a learner's goal to:

* an approved curriculum
* published lessons
* teaching
* assessment
* progress
* curriculum or lesson revision when necessary

This document describes **how the existing framework components work together**.

It does not replace the contracts that define those components.

This document defines the lifecycle for the **framework layer**.

The lifecycle below is executed inside a Learning Project, which holds the actual artifacts it produces. This repository contains no subject knowledge and no project instance.

---

# Core Lifecycle

The complete learning lifecycle is:

```text
Learning Specification
        ↓
Curriculum Proposal
        ↓
Domain Expert Critique
        ↓
Curriculum Review
        ↓
Human Approval
        ↓
Curriculum Contract
        ↓
Lesson Author
        ↓
Published Lessons
        ↓
Teacher
        ↓
Assessment
        ↓
Evidence
        ↓
Progress
        ↓
Feedback / Revision
```

The lifecycle contains two fundamentally different activities:

### Design

Determining what the learner should learn.

### Execution

Teaching and evaluating the approved learning program.

The boundary between them is the **Curriculum Contract**.

---

# The Curriculum Boundary

The most important boundary in the framework is:

```text
                 CURRICULUM DESIGN
────────────────────────────────────────────
Learning Specification
        ↓
Curriculum Proposal
        ↓
Domain Expert
        ↓
Curriculum Review
        ↓
Human Approval
        ↓
Curriculum Contract
────────────────────────────────────────────
                 LEARNING EXECUTION
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

Before the Curriculum Contract:

> The system is deciding what should be learned.

After the Curriculum Contract:

> The system is executing and teaching what was approved.

This distinction prevents teaching agents from silently redesigning the curriculum.

---

# Phase 1 — Learning Specification

The learner defines the desired learning outcome.

The Learning Specification should capture:

* subject
* primary goal
* motivation
* desired depth
* prior knowledge
* practical goals
* theoretical goals
* constraints
* learning preferences where relevant
* desired projects
* explicit exclusions
* external requirements

The specification represents the learner's intent.

It does not attempt to design the curriculum.

---

# Phase 2 — Curriculum Architecture

The Curriculum Architect transforms the Learning Specification into a Curriculum Proposal.

The Architect determines:

* scope
* learning outcomes
* modules
* dependencies
* progression
* practical application
* assessment strategy
* estimated complexity

The result is a proposal.

It is not yet authoritative.

---

# Phase 3 — Domain Expert Critique

The Domain Expert examines the proposed curriculum from a subject-matter perspective.

The Expert looks for:

* technical errors
* missing prerequisites
* incorrect sequencing
* missing critical concepts
* false completeness
* inappropriate scope
* outdated assumptions
* unnecessary complexity
* weak practical relevance

The Expert does not redesign or approve the curriculum.

The output is a critique.

---

# Phase 4 — Curriculum Review

The Curriculum Reviewer receives:

* Learning Specification
* Curriculum Proposal
* Domain Expert Critique

The Reviewer reconciles them.

The Reviewer determines:

* which expert findings matter
* which should be rejected
* which should be partially accepted
* which should become optional
* which require learner decisions
* whether the proposed curriculum satisfies the learner's goals

The Reviewer produces a recommended curriculum.

The Reviewer does not approve it.

---

# Phase 5 — Human Approval

The learner reviews the recommendation.

The learner may:

* approve
* request changes
* reject the proposal
* clarify a decision
* change goals or constraints

Human approval is the final authority over the curriculum.

Once explicitly approved, the recommendation becomes a **Curriculum Contract**.

---

# Phase 6 — Curriculum Contract

The Curriculum Contract becomes authoritative.

It defines:

* curriculum goal
* scope
* required content
* supporting content
* optional content
* excluded content
* learning outcomes
* modules
* dependencies
* progression
* practical capabilities
* assessment expectations
* approved assumptions

All downstream components must respect it.

---

# Phase 7 — Lesson Authoring

The Lesson Author converts curriculum objectives into lessons.

For each lesson, the Author:

1. Reads the current Curriculum Contract.
2. Identifies the relevant module.
3. Identifies the relevant objectives.
4. Inspects prerequisites.
5. Reviews related lessons.
6. Defines a coherent lesson boundary.
7. Writes the lesson.
8. Performs a quality check.
9. Surfaces curriculum problems when necessary.

The Lesson Author does not change the Curriculum Contract.

---

# Phase 8 — Lesson Publication

Lessons move through their lifecycle:

```text
DRAFT
  ↓
REVIEW
  ↓
PUBLISHED
  ↓
SUPERSEDED
```

The framework should not require manual approval of every lesson by default.

The purpose of human curriculum approval is to establish the learning direction.

Once the direction is approved, lesson generation should be able to operate efficiently.

Published lessons become stable learning material.

---

# Phase 9 — Teaching

The Teacher uses:

* Curriculum Contract
* Published Lessons
* learner context
* previous learning
* assessment evidence

The Teacher adapts the presentation without changing the underlying curriculum.

The Teacher may:

* explain differently
* simplify
* deepen
* provide examples
* provide exercises
* answer questions
* provide supplementary material
* revisit difficult concepts

The Teacher must not silently redefine the curriculum.

---

# Phase 10 — Assessment

Assessment provides evidence about learner progress.

Assessment should evaluate curriculum-defined objectives.

Possible evidence includes:

* explanations
* answers
* practical tasks
* projects
* configurations
* implementations
* troubleshooting
* analysis
* demonstrations

Assessment should identify not only whether an answer is correct, but where understanding is weak when possible.

### Evidence

Evidence is the learning evidence produced and recorded by Phase 10.

Evidence is a derived output of Assessment, not an agent or a separate stage with its own authority.

Evidence:

* is recorded as historical observation
* is the input consumed by Phase 11 (Progress)
* does not define what the learner must learn
* is not itself a mastery decision

The canonical relationship is:

```text
Assessment → Evidence → Progress
```

---

# Phase 11 — Progress

Evidence updates the learner's Progress state.

```text
Assessment
        ↓
Evidence
        ↓
Progress
```

Progress is an evidence-derived state and reporting function, not an additional agent.

Assessment owns the evidence. Progress interprets and reports that evidence against the approved Curriculum Contract.

Progress does not define curriculum, define assessment criteria, invent mastery criteria, or create learning requirements.

Progress should preferably be represented at the objective level.

Example:

```text
M01-O01  DEMONSTRATED
M01-O02  MASTERED
M01-O03  PRACTICING
M01-O04  NOT_STARTED
```

V1 uses exactly one Progress vocabulary:

```text
NOT_STARTED
INTRODUCED
PRACTICING
DEVELOPING
DEMONSTRATED
MASTERED
```

These states and their definitions are defined once, authoritatively, in `framework/validation/V1_CONTRACT.md` under `# Artifact States` → `## Progress`.

Progress is evidence-based.

Completing lessons does not automatically equal mastery.

---

# Phase 12 — Teaching Feedback Loop

Assessment feeds back into teaching.

```text
Lesson
  ↓
Teaching
  ↓
Practice
  ↓
Assessment
  ↓
Evidence
  ↓
Identify weakness
  ↓
Teacher intervention
  ↓
Practice
  ↓
Reassessment
```

This loop operates without changing the curriculum.

---

# Revision Loops

The framework has several different revision loops.

They must not be confused.

## Lesson Revision

```text
Published Lesson
      ↓
Problem Identified
      ↓
Lesson Revision
      ↓
Review / Validation
      ↓
New Lesson Version
```

Used when the curriculum remains correct but the learning material needs improvement.

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
Supersedes the previous version
```

Used when the approved learning program itself needs to change.

Responsibility during a curriculum revision:

```text
Architect  → creates the revision
Expert     → critiques the revision
Reviewer   → evaluates and synthesizes the revision
Human      → approves the revision
```

The Curriculum Architect owns the curriculum revision.

The Reviewer does not author the revised proposal and does not decide whether impact analysis is required for a curriculum change.

---

## Learning Specification Revision

The learner may determine that the original goal is no longer correct.

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

Changing the learner's goal may require substantial curriculum redesign.

The Learning Specification represents learner intent and is not the Curriculum Contract.

The learner decides changes to their own intent. There is no separate AI approval system for specifications.

The only approval that changes what the learner is required to learn is approval of a Curriculum Contract version, and that follows the curriculum revision process.

A specification change never silently changes the Curriculum Contract.

---

# Change Classification

When a problem is discovered, determine where it belongs.

### Teaching Problem

The curriculum and lesson are sound, but the learner needs a different explanation.

**Action:** Teacher adapts.

### Lesson Problem

The curriculum is correct, but the published lesson is insufficient or incorrect.

**Action:** Revise the lesson.

### Assessment Problem

The curriculum and lesson are appropriate, but the assessment does not measure the intended objective well.

**Action:** Revise assessment.

### Curriculum Problem

The approved curriculum itself is incomplete, incorrect, poorly sequenced, or inconsistent with the learner's goal.

**Action:** Curriculum revision process.

### Learning Specification Problem

The learner's underlying goal or constraints have changed.

**Action:** Revise the Learning Specification and reconsider the curriculum.

This classification prevents downstream components from silently fixing upstream problems.

---

# Immutability Rules

The framework follows these rules:

### Learning Specification

Mutable through explicit learner revision.

### Curriculum Proposal

Disposable and replaceable during curriculum design.

### Expert Critique

Versioned working artifact; may be superseded by a later critique.

### Curriculum Review

Versioned recommendation; not authoritative until approved.

### Curriculum Contract

Immutable by default.

Changes require the curriculum revision process.

### Published Lesson

Immutable by default.

Changes require an explicit lesson revision.

### Assessment Results

Historical evidence.

They should not be silently rewritten to hide previous results.

### Progress

May change as new evidence is collected, but previous evidence should remain recoverable when meaningful.

Progress is derived from Assessment evidence and may not create its own mastery criteria.

---

# Version Relationships

Lessons must identify which Curriculum Contract version they implement.

Example:

```text
Curriculum Contract: v1.0
Module: M03
Lesson: M03-L02
Lesson Version: 1.0
```

If the curriculum later becomes:

```text
Curriculum Contract: v2.0
```

existing lessons do not automatically become rewritten.

The framework should determine which lessons remain valid and which require revision.

---

# Curriculum Change Impact

A curriculum change may affect:

* modules
* objectives
* prerequisites
* lessons
* assessments
* learner progress
* projects
* completion criteria

Therefore curriculum changes require impact analysis.

The system should identify affected artifacts before generating replacements.

---

# Example Change

Suppose Curriculum Contract v1.0 contains:

```text
M03 — IPv4 Addressing
```

with:

```text
O1 — Explain IPv4 addressing
O2 — Calculate subnet boundaries
O3 — Design a subnet allocation
```

The learner later approves adding IPv6 as a required capability.

The system should not simply modify M03 and rewrite its lessons.

Instead:

```text
v1.0
  ↓
Change Proposal
  ↓
Impact Analysis
  ↓
Expert Review
  ↓
Curriculum Review
  ↓
Human Approval
  ↓
v2.0
```

Then affected lessons and assessments can be updated explicitly.

---

# Handling Discovered Knowledge

During teaching or assessment, the system may discover information that appears relevant but is not currently part of the curriculum.

The system must classify it.

Possible outcomes:

### Supplementary

Useful but unnecessary for achieving the curriculum.

### Prerequisite Gap

Necessary knowledge is missing.

### Curriculum Gap

An approved objective cannot reasonably be achieved without additional curriculum content.

### Future Consideration

Interesting material that does not belong in the current program.

The system must not silently convert discovered information into required curriculum.

---

# Agent Boundaries

The framework's agents have intentionally different responsibilities.

```text
Architect
  → designs

Domain Expert
  → challenges

Reviewer
  → synthesizes

Human
  → decides

Lesson Author
  → teaches through durable material

Teacher
  → adapts teaching

Assessment
  → produces evidence
```

`Evidence` and `Progress` are derived outputs and states, not agents, so they do not appear above as agents.

No component should absorb another component's responsibility merely because doing so appears convenient.

---

# Human Decision Points

Human involvement is concentrated at high-value boundaries.

The learner should make meaningful decisions about:

* learning goals
* curriculum approval
* curriculum changes
* major scope changes
* important trade-offs
* exclusions
* desired depth

The learner should not be required to manually approve every mechanical operation.

The framework is designed to maximize useful automation **without transferring ownership of the learning program to AI**.

---

# Failure Handling

When the system cannot proceed confidently, it should identify the reason.

Examples:

```text
INSUFFICIENT_INFORMATION
CURRICULUM_CONFLICT
MISSING_PREREQUISITE
TECHNICAL_UNCERTAINTY
ASSESSMENT_GAP
LESSON_GAP
OUTDATED_REFERENCE
LEARNER_DECISION_REQUIRED
```

The system should surface uncertainty rather than inventing a solution.

---

# Operational Principle

At every stage, the system should ask:

> What is my responsibility here?

and:

> What decisions belong to another stage?

This prevents role drift.

---

# End-to-End Example

This example illustrates a **Learning Project** produced from the framework.

The workflow below runs inside that project, not inside this repository.

A learner wants to become capable of designing and operating network infrastructure.

### 1. Specification

The learner defines:

* practical goal
* desired depth
* existing knowledge
* constraints
* desired projects

### 2. Architect

Produces a proposed curriculum.

### 3. Domain Expert

Finds:

* missing prerequisites
* sequencing problems
* technical issues
* important omissions

### 4. Reviewer

Produces the recommended curriculum.

### 5. Human

Approves it.

### 6. Contract

The curriculum becomes authoritative.

### 7. Lesson Author

Generates lessons for the modules.

### 8. Teacher

Teaches the lessons and adapts explanations.

### 9. Assessment

Evaluates whether the learner can actually perform the required capabilities.

Produces the evidence.

### 10. Progress

Derives demonstrated-objective state from that evidence.

### 11. Feedback

If the learner struggles:

```text
Assessment
    ↓
Teacher
    ↓
Practice
    ↓
Reassessment
```

If the lesson is inadequate:

```text
Lesson Revision
```

If the curriculum is inadequate:

```text
Curriculum Revision
```

If the learner's goal changes:

```text
Learning Specification Revision
```

Each problem goes back to the correct layer.

---

# V1 Workflow Boundary

Version 1 intentionally does not define:

* automatic curriculum generation pipelines
* automatic agent orchestration
* CLI implementation
* databases
* APIs
* web interfaces
* automatic lesson regeneration
* automatic curriculum mutation
* advanced learner modeling
* sophisticated spaced-repetition algorithms
* additional specialized agents
* Learning Project scaffolding or generation
* framework dependency resolution or package management
* automatic framework synchronization or version upgrades

These may be introduced later when real usage demonstrates a recurring need.

The framework should first validate the conceptual workflow manually.

---

# V1 Success Criteria

The workflow is successful if a learner can:

1. Define a meaningful learning goal.
2. Obtain a coherent curriculum proposal.
3. Have the curriculum challenged by a domain expert.
4. Receive a reconciled recommendation.
5. Approve a Curriculum Contract.
6. Generate useful lessons from that contract.
7. Learn through an adaptive Teacher.
8. Receive meaningful assessment.
9. Track progress against objectives.
10. Revise lessons without silently changing curriculum.
11. Revise curriculum through an explicit approval process.
12. Preserve historical decisions and learning material.

---

# Core Principle

> Every stage should make the next stage easier without taking ownership away from the stage that is responsible for the decision.

The framework separates:

**intent → design → challenge → decision → material → teaching → evidence → improvement**

so that AI can automate substantial work while the learner remains the owner of the learning program.

