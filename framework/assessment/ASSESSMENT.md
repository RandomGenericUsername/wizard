# Assessment

## Purpose

Assessment determines whether the learner has developed the knowledge, understanding, and capabilities expected by the approved curriculum.

Assessment provides evidence for learning progress.

It does not define the curriculum.

The Assessment system answers:

> Given what the learner has been expected to learn, what evidence demonstrates that they can actually do it?

---

# Role

Assessment is responsible for:

* measuring curriculum-defined learning outcomes
* evaluating learner understanding
* evaluating practical capability where required
* identifying strengths and weaknesses
* providing actionable feedback
* supporting progress decisions
* identifying learning gaps
* informing the Teacher about areas requiring reinforcement

Assessment is not responsible for:

* defining curriculum scope
* adding new curriculum requirements
* changing learning objectives
* deciding that a topic should become required
* silently modifying lessons
* replacing teaching with testing
* optimizing for scores instead of learning

---

# Evidence and Progress

Assessment owns the evidence.

Progress is derived from that evidence.

```text
Assessment → Evidence
Progress   → Derived state and report
```

Progress represents the learner's state against the approved Curriculum Contract.

Progress is an evidence-derived state and reporting function, not an additional agent or a second assessment authority.

Therefore:

```text
Progress ≠ Curriculum
Progress ≠ Assessment Criteria
Progress ≠ Mastery Criteria (unless the Curriculum Contract defines them)
```

Producing evidence does not make Assessment a curriculum designer. A progress state never becomes a curriculum requirement.

---

# Documents This Component Reads

This is a list of the documents Assessment consults, in the order it consults them.

It is not an authority hierarchy.

The authoritative hierarchy is defined in `framework/validation/V1_CONTRACT.md` under `# Authority Hierarchy`. The learner is the final authority, and the Curriculum Contract is authoritative for approved curriculum scope.

```text
MASTER.md
    ↓
AI_RULES.md
    ↓
Curriculum Contract
    ↓
Module / Objectives
    ↓
Published Lessons
    ↓
Assessment
```

The Curriculum Contract defines what the learner is expected to achieve.

Assessment determines how evidence of that achievement can be obtained.

---

# Assessment Alignment

Every meaningful assessment should map to one or more curriculum objectives.

Assessment should answer:

> What capability does this task provide evidence for?

Avoid assessments that exist merely because a particular question format is convenient.

---

# What Should Be Assessed

Assessment should prioritize meaningful capabilities.

Depending on the subject, this may include:

* recall
* explanation
* conceptual understanding
* application
* analysis
* troubleshooting
* implementation
* design
* decision-making
* comparison
* practical execution
* transfer to unfamiliar situations

The appropriate assessment type depends on the objective.

---

# Assessment Types

The framework may use different forms of assessment.

## Knowledge Check

Useful for:

* terminology
* definitions
* basic facts
* conceptual distinctions

Knowledge checks should not be overused when the curriculum expects practical capability.

---

## Explanation

The learner explains a concept in their own words.

Useful for evaluating:

* conceptual understanding
* mental models
* relationships between concepts
* reasoning

---

## Application

The learner applies a concept to a new situation.

Useful for determining whether knowledge transfers beyond memorization.

---

## Problem Solving

The learner solves a structured or open-ended problem.

Useful for:

* reasoning
* diagnosis
* analysis
* decision-making

---

## Practical Task

The learner performs an actual task.

Examples include:

* configuring a system
* implementing functionality
* analyzing data
* troubleshooting a failure
* designing a solution
* executing a procedure

Use practical assessment when the curriculum requires practical capability.

---

## Project

The learner produces a larger artifact demonstrating multiple capabilities.

Projects are appropriate when the curriculum defines integrated practical outcomes.

A project should still map back to identifiable curriculum objectives.

---

# Assessment Difficulty

Assessment difficulty should reflect the expected level of the curriculum.

Do not make assessments artificially difficult.

Difficulty should come from the capability being evaluated, not from:

* confusing wording
* irrelevant edge cases
* obscure trivia
* unnecessary complexity
* trick questions

---

# Assessment Evidence

Assessment should collect evidence sufficient to support a meaningful conclusion.

Evidence may include:

* learner answers
* explanations
* reasoning
* code
* configurations
* diagrams
* experiments
* project artifacts
* practical demonstrations
* troubleshooting processes

The type of evidence should match the capability being assessed.

---

# Formative vs Summative Assessment

The framework may distinguish between:

### Formative Assessment

Used during learning to identify weaknesses and guide teaching.

Examples:

* self-checks
* short exercises
* practice problems
* teacher questions
* small practical tasks

Formative assessment should help the learner improve.

### Summative Assessment

Used to determine whether a defined learning outcome has been sufficiently demonstrated.

Examples:

* module assessments
* practical exams
* projects
* final evaluations

The Curriculum Contract determines when meaningful summative evaluation is appropriate.

---

# Assessment Feedback

Feedback should explain:

1. What the learner demonstrated.
2. What was incorrect or incomplete.
3. Why it was incorrect or incomplete.
4. Which curriculum objective is affected.
5. What the learner should do next.

Avoid reducing feedback to:

> Correct / Incorrect.

The learner should understand how to improve.

---

# Error Classification

When possible, classify learner errors.

Useful categories include:

* factual error
* conceptual misunderstanding
* reasoning error
* procedural error
* execution error
* prerequisite gap
* careless mistake
* incomplete answer
* misconception

Classification helps the Teacher decide what intervention is appropriate.

---

# Assessment and Teaching

Assessment should feed back into teaching.

A typical loop is:

```text
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

A poor assessment result does not automatically indicate that the learner needs to repeat an entire module.

The Teacher should identify the smallest useful intervention.

---

# Mastery

This section describes the strength and quality of the evidence used to evaluate learning.

It is an assessment interpretation distinction, not a Progress vocabulary.

The framework should distinguish between:

* exposure
* practice
* demonstrated understanding
* demonstrated capability
* mastery

These terms describe increasing strength of evidence. They do not define Progress states, and they must not be used as a substitute for the Progress vocabulary.

The only Progress vocabulary is:

```text
NOT_STARTED
INTRODUCED
PRACTICING
DEVELOPING
DEMONSTRATED
MASTERED
```

defined in `framework/validation/V1_CONTRACT.md`.

A curriculum or assessment may interpret these evidence strengths when applying a Progress state, but it must not introduce additional states or replace the canonical vocabulary.

Completing a lesson does not automatically demonstrate mastery.

Likewise, answering one question correctly does not necessarily demonstrate mastery.

Mastery criteria should be defined when the curriculum requires them.

---

# Progress States

V1 uses exactly one progress vocabulary:

```text
NOT_STARTED
INTRODUCED
PRACTICING
DEVELOPING
DEMONSTRATED
MASTERED
```

These states and their definitions are defined once, authoritatively, in `framework/validation/V1_CONTRACT.md` under `# Artifact States` → `## Progress`.

Every V1 document uses this vocabulary. Alternate vocabularies are not permitted.

Progress states are derived from Assessment evidence.

The existence of a lesson, or the completion of a lesson, must not automatically produce a progress state.

Completion of a lesson must not automatically produce `DEMONSTRATED` or `MASTERED`.

A particular curriculum may define more precise criteria, but it must refine these states rather than replace them.

---

# Progress Evidence

Progress should be based on evidence rather than activity alone.

Weak evidence:

> Learner spent two hours studying networking.

Stronger evidence:

> Learner successfully configured and verified a static route in a practical task.

Time spent, lesson completion, and number of exercises may be useful context, but they should not be treated as proof of mastery by themselves.

---

# Objective-Level Progress

Progress should preferably be tracked at the objective level.

Example:

```text
Module: Network Addressing

Objective:
Explain IPv4 subnetting
Status: DEMONSTRATED

Objective:
Calculate subnet boundaries
Status: PRACTICING

Objective:
Design an address allocation plan
Status: NOT_STARTED
```

This provides more useful information than a single module percentage.

---

# Assessment Coverage

The assessment system should ensure that important curriculum objectives receive appropriate evaluation.

A curriculum may contain:

* knowledge objectives
* conceptual objectives
* practical objectives
* integrated objectives

Each should have suitable evidence.

Avoid assessing only what is easiest to test.

---

# Assessment Gaps

The Assessment system may discover that an objective is difficult or impossible to evaluate meaningfully.

Examples:

* objective is too vague
* required capability has no observable evidence
* assessment does not match the objective
* practical requirement cannot be reproduced
* mastery criteria are ambiguous

These should be surfaced as curriculum or assessment-design issues.

Do not silently redefine the objective.

---

# Assessment Integrity

Assessment should measure the intended capability.

Avoid contamination from unrelated difficulty.

For example, if the objective is:

> Configure a basic firewall rule.

The assessment should not primarily test obscure syntax unrelated to firewall reasoning.

If exact syntax is itself part of the curriculum objective, then it may appropriately be assessed.

---

# Assessment Assistance

The level of assistance provided during an assessment should depend on its purpose.

### Formative

Hints, explanations, and guidance may be appropriate.

### Summative

Assistance should follow the defined assessment rules.

The Teacher must not accidentally turn a summative assessment into a guided exercise unless the assessment explicitly allows it.

---

# Retakes

When a learner does not demonstrate an objective, reassessment may be appropriate.

A retake should generally follow:

```text
Initial Assessment
       ↓
Analyze Evidence
       ↓
Targeted Remediation
       ↓
Practice
       ↓
Reassessment
```

The learner should not simply repeat the same assessment indefinitely without addressing the underlying weakness.

---

# Reassessment

A reassessment may use:

* similar problems
* different problems
* a different context
* practical demonstration
* explanation
* transfer task

The goal is to determine whether the learner developed the capability rather than memorized the previous answer.

---

# Assessment Security

Where assessment integrity matters, the system may restrict:

* access to answers
* hints
* external references
* collaboration
* tool usage
* time
* repeated attempts

These restrictions should only exist when relevant to the purpose of the assessment.

The framework should not impose artificial restrictions by default.

---

# External References

Whether external references are allowed should be determined by the assessment.

Some real-world capabilities require reference material.

For example, professional technical work often involves documentation lookup.

If the curriculum expects learners to work effectively with documentation, allowing references may be more authentic than banning them.

---

# Projects

Projects should evaluate integrated capabilities.

A project should define:

* objective(s)
* expected artifact
* constraints
* required capabilities
* evaluation criteria
* acceptable resources
* evidence requirements

Projects should not become unbounded assignments.

---

# Rubrics

When useful, assessments may use rubrics.

A rubric should define observable criteria.

Example:

```text
Criterion: Diagnose connectivity failure

Excellent:
Identifies the failure domain, gathers appropriate evidence,
tests hypotheses systematically, and explains the root cause.

Developing:
Identifies some relevant evidence but tests hypotheses
inconsistently or reaches an incomplete conclusion.

Insufficient:
Cannot establish a plausible failure domain or explain
the observed behavior.
```

Rubrics should evaluate capability rather than stylistic preference.

---

# AI-Generated Assessment

AI may generate assessment material when useful.

AI-generated assessments must:

* map to approved objectives
* respect assessment requirements
* avoid introducing new curriculum
* use appropriate difficulty
* avoid fabricated facts
* provide reliable evaluation criteria

AI should not generate arbitrary tests simply to increase activity.

---

# Assessment Adaptation

Assessment may adapt to the learner when the assessment type permits it.

For formative assessment, the system may adjust:

* difficulty
* hints
* examples
* number of practice items
* context

For summative assessment, adaptation must follow the defined assessment rules.

Adaptive assessment must not make different learners demonstrate fundamentally different curriculum requirements unless the curriculum explicitly permits it.

---

# Relationship to the Teacher

The Teacher uses assessment evidence to guide instruction.

Assessment should report useful information such as:

```text
Objective
Evidence
Result
Confidence
Observed weakness
Recommended next action
```

The Teacher then determines the appropriate teaching intervention.

Assessment does not prescribe the entire teaching strategy.

---

# Relationship to Curriculum

Assessment evaluates the Curriculum Contract.

It must not become a hidden curriculum-design mechanism.

If an assessment repeatedly reveals that an objective is:

* impossible to teach effectively
* impossible to assess meaningfully
* missing necessary prerequisites
* incorrectly scoped
* ambiguous

the issue should be surfaced for curriculum review.

The assessment system may recommend change.

It may not silently make the change.

---

# Relationship to Lessons

Lessons provide the material used to prepare the learner.

Assessment may reveal problems in lessons.

For example:

> Learners repeatedly fail objective M03-O2 despite adequate prerequisite knowledge.

This may indicate a lesson problem.

The appropriate response may be:

1. inspect learner evidence
2. inspect the relevant lesson
3. determine whether teaching material is insufficient
4. revise the lesson if appropriate
5. reassess

Do not automatically change the curriculum.

---

# Progress Reporting

Progress reports should be useful for decision-making.

A progress report may include:

```text
Curriculum: Network Infrastructure
Contract Version: 1.0

Module 1:
  Objectives demonstrated: 4/4

Module 2:
  Objectives demonstrated: 3/5

Current focus:
  IPv4 subnetting

Weak areas:
  - subnet boundary calculation
  - address allocation planning

Recommended action:
  targeted practice before continuing
```

Avoid presenting false precision.

A statement such as:

> 67.3% mastered

may imply more certainty than the evidence supports.

Prefer meaningful objective-level evidence.

---

# Completion Criteria

A curriculum may define completion criteria such as:

* all required objectives demonstrated
* required practical capabilities demonstrated
* required assessments completed
* required project completed
* minimum performance thresholds met

Completion criteria must come from the Curriculum Contract.

The Assessment system must not invent them.

---

# Quality Checklist

Before finalizing an assessment, verify:

### Alignment

* [ ] Does the assessment map to approved objectives?
* [ ] Does it evaluate the intended capability?
* [ ] Does it remain within curriculum scope?

### Validity

* [ ] Does success actually provide evidence of the objective?
* [ ] Is irrelevant difficulty minimized?
* [ ] Are evaluation criteria observable?

### Difficulty

* [ ] Is difficulty appropriate?
* [ ] Are there no unnecessary tricks?
* [ ] Does the task require meaningful reasoning or capability?

### Feedback

* [ ] Can meaningful feedback be produced?
* [ ] Can weaknesses be identified?
* [ ] Can the Teacher act on the evidence?

### Boundaries

* [ ] Does the assessment avoid introducing new curriculum requirements?
* [ ] Does it respect assessment rules?
* [ ] Does it avoid silently changing mastery criteria?

---

# Assessment Lifecycle

A typical assessment lifecycle is:

```text
Curriculum Objective
        ↓
Assessment Design
        ↓
Assessment
        ↓
Evidence
        ↓
Evaluation
        ↓
Feedback
        ↓
Progress Update
        ↓
Teacher Intervention
        ↓
Reassessment when needed
```

---

# Core Principle

> Assessment does not exist to produce scores. It exists to produce evidence about learning.

The purpose of that evidence is to help the learner and Teacher understand what has been learned, what has not, and what should happen next.

