# Learning Specification

**Version:** 1.0
**Status:** Contract

---

## 1. Purpose

The Learning Specification describes what the learner wants to achieve.

It is the input to the curriculum-design process.

It describes the learner's desired destination without prescribing the curriculum that will be used to reach it.

The Learning Specification should contain enough information for the Curriculum Architect to design a meaningful curriculum, while avoiding unnecessary manual curriculum design by the learner.

---

## 2. Core Principle

The learner describes:

> **Where do I want to go, why, and under what constraints?**

The Curriculum Architect determines:

> **What should I learn, and in what order, to get there?**

The Learning Specification must therefore describe goals and constraints, not attempt to become a manually authored curriculum.

---

## 3. Required Information

A valid Learning Specification must contain:

### 3.1 Subject

What general domain does the learner want to study?

Examples:

* Network Infrastructure
* Web Development
* Rust
* Financial Markets
* Electronics

The subject may initially be broad.

---

### 3.2 Primary Goal

What does the learner ultimately want to be able to do?

The goal should describe an outcome rather than merely naming a topic.

Weak:

> Learn networking.

Better:

> Understand and build network infrastructure for small and medium-sized environments.

---

### 3.3 Motivation

Why does the learner want to achieve this goal?

Motivation helps the Architect understand the intended context and make appropriate scope decisions.

Examples:

* Career development
* Build personal projects
* Understand an existing system
* Prepare for professional work
* Academic study
* Personal curiosity

---

### 3.4 Desired Depth

The learner should indicate the approximate depth they want.

Suggested levels:

* **Familiarity** — recognize concepts and understand basic terminology.
* **Fundamental** — understand core concepts and explain them.
* **Practical** — independently perform common tasks.
* **Advanced** — handle complex real-world problems.
* **Expert-oriented** — develop deep theoretical and practical understanding.

This is an initial target, not a guarantee of the final curriculum size.

---

## 4. Optional Information

The learner may provide any of the following.

### 4.1 Prior Knowledge

What does the learner already know?

This may include:

* concepts;
* technologies;
* practical experience;
* previous education;
* related subjects.

The learner does not need to provide a complete knowledge inventory.

The system may identify gaps later.

---

### 4.2 Practical Goals

Specific things the learner wants to be able to accomplish.

Examples:

* Configure a network.
* Build a web application.
* Deploy a service.
* Diagnose failures.
* Design a system.
* Read technical documentation.

Practical goals are especially useful when the subject is skill-oriented.

---

### 4.3 Theoretical Goals

Concepts the learner particularly wants to understand.

Examples:

* Why a system works.
* Underlying mechanisms.
* Mathematical foundations.
* Architectural principles.
* Trade-offs between approaches.

---

### 4.4 Constraints

Anything that should influence curriculum design.

Examples:

* Available time.
* Available hardware.
* Available software.
* Operating system.
* Budget.
* Geographic limitations.
* Professional requirements.
* Accessibility requirements.

Constraints should describe real limitations, not prescribe the curriculum itself.

---

### 4.5 Preferred Learning Style

Optional preferences such as:

* theory first;
* practice first;
* projects;
* exercises;
* visual explanations;
* documentation-driven learning;
* code-first learning;
* mathematical derivations;
* experimentation.

These are preferences, not rigid rules.

The Teacher may adapt them later.

---

### 4.6 Desired Projects

Projects the learner would eventually like to build.

Projects are goals or evidence of application, not necessarily curriculum items.

The Architect determines where and whether they fit.

---

### 4.7 Explicit Exclusions

Topics the learner explicitly does not want included.

Examples:

> I want to learn web development, but I am not interested in mobile development.

Explicit exclusions are learner constraints.

They must be preserved by downstream components unless the learner explicitly decides to change them.

AI may identify that an exclusion conflicts with an essential prerequisite, explain why the prerequisite matters, and recommend a decision.

AI must not override the exclusion itself.

If an exclusion conflicts with an essential prerequisite, the conflict must be surfaced to the learner:

```text
AI identifies conflict
        ↓
AI explains conflict
        ↓
AI recommends options
        ↓
Learner decides
```

AI must never resolve an exclusion conflict by overriding the exclusion.

---

### 4.8 External Requirements

Requirements imposed by something outside the learner.

Examples:

* A job requirement.
* A certification.
* A university course.
* A professional standard.
* A project requirement.

External requirements should be identified separately from personal goals.

---

## 5. Specification Structure

A Learning Specification should normally use the following structure:

```markdown
# Learning Specification

## Subject

[Subject]

## Primary Goal

[What I want to be able to do]

## Motivation

[Why I want to learn this]

## Desired Depth

[Target depth]

## Prior Knowledge

[What I already know]

## Practical Goals

- [Goal]
- [Goal]

## Theoretical Goals

- [Goal]
- [Goal]

## Constraints

- [Constraint]
- [Constraint]

## Learning Preferences

- [Preference]
- [Preference]

## Desired Projects

- [Project]
- [Project]

## Explicit Exclusions

- [Exclusion]

## External Requirements

- [Requirement]
```

Sections that do not apply may be omitted.

---

## 6. Quality Requirements

A Learning Specification should be:

### Clear

The intended outcome should be understandable.

### Outcome-oriented

It should describe what the learner wants to achieve, not merely list technologies or topics.

### Honest

The learner should not need to pretend to know more or less than they do.

### Flexible

It should allow incomplete information.

### Non-prescriptive

It should avoid manually defining the curriculum unless the learner intentionally provides a requirement.

### Actionable

The Curriculum Architect should be able to use it to produce a curriculum proposal.

---

## 7. What the Specification Must Not Do

The Learning Specification should not normally contain:

* a complete curriculum;
* a detailed lesson sequence;
* lesson content;
* assessment questions;
* teaching scripts;
* implementation details for the learning framework.

Those belong to later artifacts.

The learner may provide suggestions, but the Architect is responsible for transforming the learning goal into a curriculum.

---

## 8. AI Behavior

When helping create a Learning Specification, AI should:

1. Extract the learner's actual goals.
2. Ask only for information that materially affects curriculum design.
3. Detect ambiguity that could significantly change the resulting curriculum.
4. Avoid forcing the learner through an unnecessarily large questionnaire.
5. Infer reasonable structure from natural-language input when possible.
6. Clearly identify assumptions when they materially affect the result.
7. Never silently convert an assumption into a learner requirement.

If sufficient information exists, AI should produce the specification rather than continuing to ask questions indefinitely.

---

## 9. Revision

The Learning Specification may change before curriculum approval.

Once a curriculum has been approved, changing the Learning Specification may have consequences for the Curriculum Contract.

If a specification change affects the approved curriculum, the system should identify the affected decisions and propose a curriculum revision.

It must not silently modify the approved curriculum.

---

## 10. Relationship to Other Artifacts

The Learning Specification is consumed primarily by:

**Curriculum Architect**

It informs:

**Domain Expert**

**Curriculum Reviewer**

**Teacher**

**Assessment**

The Learning Specification does not directly authorize changes to the curriculum.

---

## 11. Example

A learner might provide:

```markdown
# Learning Specification

## Subject

Network Infrastructure

## Primary Goal

I want to understand how modern computer networks work and eventually be able to design, configure, troubleshoot, and operate networks independently.

## Motivation

I want practical infrastructure knowledge that I can use for personal projects and professional work.

## Desired Depth

Advanced

## Prior Knowledge

I understand basic IP addresses, Ethernet, and common networking terminology, but I do not have a systematic understanding of networking.

## Practical Goals

- Configure networks.
- Troubleshoot connectivity problems.
- Understand routing.
- Work with VLANs.
- Understand network security.
- Build a realistic lab environment.

## Theoretical Goals

- Understand how network protocols work.
- Understand why routing works.
- Understand how different network layers interact.

## Constraints

- I want to use a home lab where possible.
- I prefer open-source tools.

## Learning Preferences

- Explain concepts from first principles.
- Combine theory with practical experimentation.
- Use realistic projects.

## Desired Projects

- Build a virtualized network lab.
- Design a small enterprise network.

## Explicit Exclusions

- None.

## External Requirements

- None.
```

The learner has defined the **destination and constraints**.

They have not manually designed the curriculum.

That distinction is fundamental to the framework.


