# Learning Framework

**Version:** 1.0  
**Status:** Approved Architecture


## 1. Purpose

The Learning Framework is a reusable system for designing, generating, teaching, and maintaining structured learning programs across arbitrary subjects.

The framework exists to solve a recurring problem:

> Creating a high-quality learning environment for every new subject currently requires manually designing the scope, roadmap, curriculum, lessons, teaching methodology, and supporting material from scratch.

The framework moves the repetitive curriculum-design work to AI while preserving human ownership and curation of the learning experience.

The framework must support radically different subjects without being tied to a particular domain.

Examples include:

* Web development
* Network infrastructure
* Programming languages
* Trading
* Systems administration
* Mathematics
* Other technical or non-technical subjects

The subject changes. The learning machinery does not.

---

# 2. Core Philosophy

The framework is based on five principles.

## 2.1 Human ownership

The learner remains the ultimate authority over what they want to learn and what constitutes an acceptable curriculum.

AI assists with design and execution but does not independently decide the learner's educational goals.

---

## 2.2 AI-assisted, not AI-owned

AI should remove repetitive intellectual and organizational work without removing meaningful human control.

The system should make it inexpensive for the learner to curate a curriculum rather than attempting to eliminate curation entirely.

---

## 2.3 Separation of concerns

Different responsibilities must be assigned to different components.

In particular:

* Designing a curriculum is different from knowing a domain.
* Knowing a domain is different from reviewing a curriculum.
* Generating lessons is different from teaching lessons.
* Teaching is different from assessing learning.

The framework must preserve these boundaries.

---

## 2.4 Stable learning material

Once the learner approves a curriculum and its lessons, those artifacts become stable learning material.

AI must not silently rewrite approved curriculum or lessons.

Changes require an explicit request or an explicit framework workflow.

---

## 2.5 Iterative improvement

The framework itself is expected to evolve.

When using the system reveals a recurring weakness, the framework should be improved rather than repeatedly compensating for that weakness manually inside individual subjects.

---

# 3. Problem Definition

For each major subject, the learner traditionally has to perform many of the same tasks:

1. Define the learning goal.
2. Define the scope.
3. Determine prerequisites.
4. Design a roadmap.
5. Decompose the roadmap into lessons.
6. Determine lesson ordering.
7. Write or generate lesson content.
8. Design exercises and projects.
9. Define teaching behavior.
10. Track progress.
11. Maintain the material.

Repeating this process for every subject does not scale.

The Learning Framework provides a reusable process for performing these tasks while retaining human approval at important decision points.

---

# 4. Goals

The v1 framework must:

* Allow a learner to describe what they want to learn without manually designing the entire curriculum.
* Generate a proposed learning specification.
* Generate a proposed curriculum from that specification.
* Critically evaluate the curriculum using independent domain knowledge.
* Review and reconcile the curriculum against the learner's goals.
* Require human approval before a curriculum becomes authoritative.
* Generate structured lessons from an approved curriculum.
* Provide a reusable teacher capable of teaching different subjects.
* Support assessment and progress tracking.
* Keep approved curriculum and lessons stable unless explicitly changed.
* Allow the same framework to support many unrelated subjects.
* Keep the learner's required curation effort focused on high-value decisions.

---

# 5. Non-Goals

The v1 framework does not attempt to:

* Automatically determine what a learner should value.
* Eliminate human curriculum curation.
* Guarantee perfect curricula.
* Guarantee perfect factual accuracy.
* Replace domain experts or authoritative sources.
* Automatically modify approved learning material.
* Build a universal autonomous teacher that independently changes the curriculum.
* Optimize for the largest possible number of AI agents.
* Solve every possible learning modality in v1.
* Fully automate every interaction with external educational resources.

The framework should prefer a small number of clearly defined components over unnecessary complexity.

---

# 6. Core Concepts

## 6.1 Learning Specification

The Learning Specification describes what the learner wants from a subject.

It may contain:

* Learning goals
* Motivation or intended use
* Current knowledge
* Desired competency
* Scope
* Explicit exclusions
* Desired depth
* Practical/theoretical balance
* Preferred tools or environments
* Constraints
* Learning preferences

The Learning Specification describes the learner's intent.

It does not prescribe the final curriculum.

---

## 6.2 Curriculum

The Curriculum describes what the learner will learn and in what progression.

It contains the educational structure derived from the Learning Specification.

The curriculum may include:

* Modules
* Topics
* Lessons
* Prerequisites
* Learning objectives
* Projects
* Exercises
* Assessments
* Dependencies
* Expected progression

The curriculum is subject to review and human approval.

---

## 6.3 Lesson

A Lesson is a discrete unit of learning material belonging to an approved curriculum.

A lesson should have enough structured information for the framework to understand:

* What it teaches
* Why it exists
* What it requires
* What the learner should be able to do afterward
* How it relates to other lessons
* How understanding can be assessed

The actual lesson content may contain explanations, examples, demonstrations, exercises, and other educational material.

---

## 6.4 Teacher

The Teacher is the interactive learning interface between the learner and the approved learning material.

The Teacher determines how to teach the material without independently redefining what the curriculum is.

The Teacher may:

* Explain concepts
* Ask questions
* Adapt explanations
* Provide examples
* Give exercises
* Identify misunderstandings
* Revisit prerequisites
* Assess understanding
* Adjust teaching pace

The Teacher must respect the approved curriculum.

---

## 6.5 Domain Expert

The Domain Expert provides subject-specific knowledge and acts as an adversarial critic of the proposed curriculum.

The Domain Expert's purpose is not to design the curriculum.

Its purpose is to identify problems that a generic curriculum architect may miss.

It should search for:

* Missing concepts
* Incorrect dependencies
* Hidden prerequisites
* Incorrect sequencing
* Dangerous simplifications
* Conceptual gaps
* Redundancy
* Scope problems
* Theory/practice disconnects
* Important domain-specific considerations

The Domain Expert must challenge the proposed curriculum rather than simply validate it.

---

# 7. System Architecture

The v1 system consists of the following primary components:

```text
                    Learner
                       │
                       ▼
             Learning Specification
                       │
                       ▼
              Curriculum Architect
                       │
                       ▼
                 Domain Expert
                 (adversarial)
                       │
                       ▼
              Curriculum Reviewer
                       │
                       ▼
                Human Approval
                       │
                       ▼
                 Lesson Author
                       │
                       ▼
              Approved Lessons
                       │
                       ▼
                    Teacher
                       │
                       ▼
             Assessment / Progress
```

Each component has a defined responsibility.

No component should silently assume the responsibilities of another component.

---

# 8. Component Responsibilities

## 8.1 Learning Specification

Responsible for representing learner intent.

It answers:

> What does the learner want to accomplish?

It does not decide the curriculum independently.

---

## 8.2 Curriculum Architect

Responsible for transforming the Learning Specification into a proposed curriculum.

It answers:

> Given the learner's goals, what should the learning path look like?

The Architect is responsible for:

* Curriculum structure
* Topic decomposition
* Ordering
* Prerequisites
* Learning progression
* Appropriate depth
* Practical components
* Projects
* Assessments

The Architect must remain aligned with the learner's stated scope.

---

## 8.3 Domain Expert

Responsible for adversarial domain analysis.

It answers:

> If I were an expert in this subject, what is wrong, missing, misleading, or questionable about this proposed curriculum?

The Expert must not blindly accept the Architect's structure.

The Expert must not independently redefine the learner's goals.

---

## 8.4 Curriculum Reviewer

Responsible for evaluating the curriculum using:

* Learning Specification
* Proposed Curriculum
* Domain Expert critique

It answers:

> Given the learner's goals and the available domain critique, what should the curriculum actually look like?

The Reviewer may:

* Accept Architect decisions.
* Accept Expert criticism.
* Reject Expert criticism when it conflicts with the learner's scope.
* Request curriculum changes.
* Identify unresolved issues.
* Produce a revised curriculum proposal.

The Reviewer does not have final authority.

---

## 8.5 Human Approval

The learner is the final authority over the curriculum.

A curriculum does not become authoritative merely because AI agents agree.

The learner must explicitly approve it.

Human approval establishes the boundary between:

```text
AI-generated proposal
```

and:

```text
learner-approved curriculum
```

---

## 8.6 Lesson Author

Responsible for transforming an approved curriculum into learning material.

The Lesson Author must follow the approved curriculum.

It must not silently introduce major curriculum changes.

If lesson generation exposes a curriculum problem, the issue should be surfaced rather than silently changing the curriculum.

---

## 8.7 Teacher

Responsible for delivering the approved learning experience interactively.

The Teacher must distinguish between:

* Approved curriculum material
* Supplementary explanations
* Temporary teaching aids
* Proposed curriculum changes

The Teacher must not silently modify the authoritative curriculum.

---

## 8.8 Assessment / Progress

Responsible for determining and recording evidence of learning.

Assessment may include:

* Questions
* Exercises
* Practical tasks
* Projects
* Demonstrations
* Other appropriate evidence

Progress represents the learner's demonstrated state rather than merely the number of lessons viewed.

---

# 9. Subject Lifecycle

Every subject follows the same conceptual lifecycle.

```text
IDEA
  │
  ▼
LEARNING SPECIFICATION
  │
  ▼
CURRICULUM PROPOSAL
  │
  ▼
DOMAIN EXPERT CRITIQUE
  │
  ▼
CURRICULUM REVIEW
  │
  ▼
HUMAN APPROVAL
  │
  ▼
LESSON GENERATION
  │
  ▼
PUBLISHED LEARNING MATERIAL
  │
  ▼
TEACHING
  │
  ▼
ASSESSMENT
  │
  ▼
PROGRESS
```

The lifecycle may contain revision loops.

For example:

```text
Curriculum
    ↓
Expert critique
    ↓
Reviewer
    ↓
Issues remain
    ↓
Architect revision
    ↓
Expert critique
    ↓
Reviewer
    ↓
Human approval
```

The exact number of iterations is not fixed.

---

# 10. Human Approval Gates

Human approval is required at meaningful boundaries.

At minimum, v1 requires approval of:

1. The Learning Specification when necessary.
2. The final Curriculum.
3. Explicit modifications to approved learning material.

The purpose of approval is not to make the learner manually inspect everything.

The purpose is to ensure the learner controls the decisions that materially affect their education.

The system should therefore optimize for:

> Maximum useful AI work before the human approval point.

---

# 11. Immutability and Ownership

Approved curriculum and lessons are authoritative learning artifacts.

AI must not silently modify them.

Changes require an explicit action.

For example:

```text
Approved Lesson
      │
      ├── Teach
      │
      └── Explicit improvement request
                 │
                 ▼
          Proposed revision
                 │
                 ▼
             Approval
                 │
                 ▼
          Updated lesson
```

A teacher discovering that additional material may be useful must not silently insert it into the curriculum.

It should instead identify the issue as one of:

* Supplementary material
* Missing prerequisite
* Curriculum gap
* Requested curriculum modification

The learner decides how to proceed.

---

# 12. AI Autonomy Boundaries

AI may autonomously perform work within its assigned responsibility.

AI may not silently cross responsibility boundaries.

For example:

### Architect

May design a curriculum.

May not decide that the learner's stated goals are irrelevant.

### Domain Expert

May identify missing domain concepts.

May not force those concepts into the curriculum.

### Reviewer

May reconcile Architect and Expert feedback.

May not override the learner's final approval.

### Lesson Author

May generate lessons.

May not silently redesign the curriculum.

### Teacher

May adapt explanations and teaching strategies.

May not silently redefine the learning objectives.

---

# 13. Adversarial Design

The framework intentionally introduces disagreement into curriculum creation.

The Architect is expected to produce a coherent curriculum.

The Domain Expert is expected to challenge it.

The Reviewer is expected to reconcile the disagreement.

This creates a process closer to:

```text
Proposal
   ↓
Challenge
   ↓
Reconciliation
   ↓
Human decision
```

rather than:

```text
AI generates curriculum
   ↓
AI approves its own curriculum
```

The adversarial process exists to reduce plausible-looking but incomplete curricula.

---

# 14. Curriculum Contract

Once a curriculum is approved, it becomes the subject's authoritative Curriculum Contract.

The contract establishes at minimum:

* Learning objectives
* Scope
* Exclusions
* Curriculum structure
* Expected depth
* Major learning dependencies
* Approved practical emphasis
* Other decisions explicitly made by the learner

Future AI components must treat this contract as authoritative.

If a component discovers a reason to change it, the change must be surfaced as a proposal.

---

# 15. Supplementary Material

Not every useful piece of knowledge needs to become part of the authoritative curriculum.

The system must distinguish between:

```text
CURRICULUM
```

and:

```text
SUPPLEMENTARY MATERIAL
```

Supplementary material may be introduced by the Teacher when useful without modifying the curriculum.

Examples include:

* Additional examples
* Alternative explanations
* Historical context
* Optional exercises
* Additional references
* Temporary remediation

This allows the Teacher to be flexible without corrupting the curriculum.

---

# 16. Framework vs Subject

The framework itself must remain subject-agnostic.

The framework defines:

* Processes
* Roles
* Responsibilities
* Artifact relationships
* Approval mechanisms
* Teaching methodology
* Assessment methodology
* Lifecycle rules

A subject defines:

* Domain knowledge
* Learning objectives
* Scope
* Curriculum
* Lessons
* Exercises
* Projects
* References
* Domain-specific expert knowledge

Therefore:

```text
FRAMEWORK
    +
SUBJECT
    =
LEARNING ENVIRONMENT
```

The framework should be reusable without modification when a new subject is created.

---

# 17. Framework Evolution

The framework is itself versioned conceptually.

V1 should remain intentionally conservative.

New components should be introduced only when actual use demonstrates a recurring need that cannot be handled by existing responsibilities.

The default response to a problem should be:

1. Determine which existing component owns the problem.
2. Improve that component.
3. Only create a new component if the responsibility is genuinely distinct.

The framework should avoid agent proliferation.

---

# 18. V1 Scope

V1 consists of:

### Core process

```text
Learning Specification
→ Curriculum Architect
→ Domain Expert
→ Curriculum Reviewer
→ Human Approval
→ Lesson Author
→ Teacher
→ Assessment / Progress
```

### Core properties

* Human curriculum ownership
* Adversarial curriculum review
* Explicit approval
* Stable approved learning material
* Reusable teacher
* Subject-agnostic architecture
* Explicit AI responsibility boundaries
* Support for supplementary material
* Iterative framework improvement

V1 does not require sophisticated automation.

The first implementation may be entirely file- and prompt-based.

Automation should be introduced only after the workflow has been validated manually.

---

# 19. V1 Success Criteria

The framework succeeds if a learner can start a new subject without manually performing the majority of curriculum-design work.

A successful workflow should look approximately like:

```text
"I want to learn X."
        ↓
Answer a small number of questions
        ↓
Review generated learning specification
        ↓
Review proposed curriculum
        ↓
Review AI's adversarial analysis
        ↓
Approve curriculum
        ↓
AI generates learning material
        ↓
Start learning
```

The learner should spend their time primarily on:

* Defining what they want.
* Making meaningful scope decisions.
* Reviewing important curriculum decisions.
* Learning.

They should spend substantially less time on:

* Manually decomposing subjects.
* Creating dozens of lesson files.
* Rewriting the same teacher instructions.
* Recreating the same repository structure.
* Performing repetitive curriculum-design work.

---

# 20. Guiding Principle

The framework should not attempt to remove the learner from the educational process.

It should remove the **unnecessary administrative and curriculum-engineering burden** surrounding the educational process.

The desired outcome is:

> **The learner curates the destination.
> AI helps construct the road.
> The learner approves the road.
> AI helps teach the journey.**

