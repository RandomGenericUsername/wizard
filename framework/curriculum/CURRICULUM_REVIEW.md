# Curriculum Review

**Version:** 1.0
**Status:** Contract

---

## 1. Purpose

The Curriculum Review is the synthesis stage between curriculum design and human approval.

It evaluates:

* the Learning Specification;
* the Curriculum Proposal;
* the Domain Expert Critique.

Its purpose is to determine what the proposed curriculum should look like **before the learner makes the final approval decision**.

The Curriculum Reviewer asks:

> **Given the learner's goals, the proposed curriculum, and the expert's critique, what curriculum should we recommend to the learner?**

The Reviewer produces a recommendation.

The learner remains the final authority.

---

## 2. Core Principle

The Reviewer is a **decision-making synthesis role**, not simply another critic.

It must:

1. understand the learner's objectives;
2. evaluate the Architect's reasoning;
3. evaluate the Expert's findings;
4. resolve disagreements where possible;
5. identify unresolved decisions;
6. produce a coherent recommended curriculum.

The Reviewer must not blindly accept either the Architect or the Domain Expert.

---

## 3. Inputs

The Reviewer receives:

* Learning Specification;
* Curriculum Proposal;
* Domain Expert Critique.

The Reviewer may use supporting evidence when necessary to resolve factual or domain questions.

---

## 4. Responsibilities

The Reviewer is responsible for determining whether:

### 4.1 The curriculum serves the learner's goals

The curriculum should remain aligned with the learner's:

* primary goal;
* desired depth;
* practical goals;
* theoretical goals;
* constraints;
* exclusions;
* external requirements.

---

### 4.2 Expert findings matter

Each significant Expert finding should be evaluated.

The Reviewer should determine whether it should result in:

* a curriculum change;
* an optional addition;
* clarification;
* no change;
* a question for the learner.

The Reviewer must not automatically implement every Expert recommendation.

---

### 4.3 The curriculum is coherent

The final recommendation should have:

* logical progression;
* appropriate prerequisites;
* coherent scope;
* appropriate depth;
* meaningful practical application;
* clear learning outcomes.

---

### 4.4 Trade-offs are explicit

Curriculum design often involves trade-offs.

Examples:

* breadth vs depth;
* theory vs practice;
* speed vs completeness;
* foundational knowledge vs immediate application;
* general principles vs tool-specific knowledge.

When a meaningful trade-off exists, the Reviewer should make it explicit.

---

## 5. Review Process

The Reviewer should follow this general process.

### Step 1 — Validate the Learning Specification

Confirm that the learner's goals and constraints are sufficiently clear.

If a major ambiguity prevents responsible curriculum design, identify it.

---

### Step 2 — Evaluate the Curriculum Proposal

Determine whether the proposed structure actually serves the Learning Specification.

Check:

* scope;
* outcomes;
* modules;
* dependencies;
* progression;
* practical work;
* assessment strategy.

---

### Step 3 — Evaluate Expert Findings

For each significant finding:

1. understand the claim;
2. evaluate its reasoning or evidence;
3. determine its relevance to the learner;
4. determine its impact on the curriculum;
5. decide how it should affect the recommendation.

---

### Step 4 — Resolve Conflicts

The Architect and Expert may reasonably disagree.

The Reviewer should determine whether:

* the Architect is correct;
* the Expert is correct;
* both contain useful perspectives;
* the issue depends on learner preference;
* more information is required.

The Reviewer should not hide meaningful disagreements.

---

### Step 5 — Produce the Recommended Curriculum

The Reviewer should produce a coherent curriculum recommendation rather than merely a list of suggested edits.

The recommendation should be understandable on its own.

---

### Step 6 — Identify Human Decisions

Some decisions may depend on learner preference rather than objective correctness.

These should be explicitly presented to the learner.

---

## 6. Finding Resolution

Each significant Expert finding should receive a disposition.

Use:

### ACCEPT

The finding is valid and should affect the curriculum.

### PARTIALLY_ACCEPT

The finding is valid, but only part of the recommendation should be incorporated.

### REJECT

The finding does not justify a curriculum change.

The reason must be stated.

### OPTIONAL

The finding is useful but should not become required curriculum material.

### DEFER

The issue requires a learner decision or additional information.

---

## 7. Review Finding Structure

Use:

```markdown id="wz8b3j"
### Review Finding [ID]

**Expert Finding:** [Expert finding ID]

**Disposition:** [ACCEPT | PARTIALLY_ACCEPT | REJECT | OPTIONAL | DEFER]

**Reasoning:**

[Why this disposition was chosen]

**Curriculum Impact:**

[What should change, if anything]

**Learner Decision Required:**

[Yes | No]

[If yes, explain the decision]
```

---

## 8. Recommended Curriculum

The review must contain a recommended curriculum.

It should not merely say:

> "The Architect should revise Module 3."

Instead, it should describe the resulting recommended structure.

The recommendation should contain:

* curriculum goal;
* scope;
* learning outcomes;
* modules;
* module objectives;
* major concepts;
* prerequisites;
* progression;
* practical application;
* assessment strategy;
* important assumptions.

The structure should remain consistent with the Curriculum Proposal contract.

---

## 9. Human Decision Points

The Reviewer must identify decisions that cannot reasonably be made without learner input.

Examples:

* choosing between substantially different scopes;
* accepting a significant increase in curriculum length;
* including a topic the learner explicitly excluded;
* choosing between competing goals;
* resolving an ambiguous external requirement.

For each such issue:

```markdown id="n0q1sh"
### Human Decision [ID]

**Decision:**

[What must be decided]

**Why It Matters:**

[Why the decision affects the curriculum]

**Option A:**

[Description]

**Option B:**

[Description]

**Recommendation:**

[Recommended option, if appropriate]

**Consequence:**

[What changes depending on the decision]
```

The Reviewer may recommend an option but must not make the learner's decision on their behalf.

---

## 10. Recommended Curriculum Status

The review should conclude with one of:

```text id="j8r7wa"
READY_FOR_APPROVAL
REQUIRES_LEARNER_DECISION
REQUIRES_REVISION
INSUFFICIENT_INFORMATION
```

### READY_FOR_APPROVAL

The Reviewer believes the curriculum is sufficiently defined and no unresolved learner decisions materially affect it.

### REQUIRES_LEARNER_DECISION

The curriculum contains one or more meaningful decisions that require the learner.

### REQUIRES_REVISION

The Architect should revise the proposal before it can reasonably be presented for approval.

### INSUFFICIENT_INFORMATION

The available information is insufficient to responsibly evaluate or construct the curriculum.

---

## 11. What the Reviewer Must Not Do

The Reviewer must not:

* approve the curriculum on behalf of the learner;
* silently override explicit learner constraints;
* blindly accept the Domain Expert's recommendations;
* blindly accept the Architect's proposal;
* redefine the learner's goals;
* silently expand curriculum scope;
* silently remove important curriculum requirements;
* generate lessons;
* modify published lessons;
* author or rewrite the Curriculum Proposal;
* turn optional material into required material.

The Reviewer may recommend that optional material become required curriculum.

Making it required is a curriculum change, and it requires the appropriate human approval.

---

## 12. Human Approval Boundary

The Review is the final AI-generated curriculum recommendation.

The next step is **Human Approval**.

The learner may:

* approve the recommendation;
* request changes;
* reject the recommendation;
* modify the scope;
* request another review.

Only after explicit approval does the recommendation become the authoritative Curriculum Contract.

---

## 13. Curriculum Contract Creation

When the learner approves the recommended curriculum, the approved version becomes the Curriculum Contract.

The Curriculum Contract must preserve:

* approved scope;
* approved learning outcomes;
* approved progression;
* approved required modules;
* approved requirements;
* explicit exclusions;
* relevant learner decisions.

AI components must treat the resulting contract as authoritative until the learner explicitly approves a revision.

---

## 14. Revision

If the learner requests changes to the recommendation itself, the Reviewer revises the recommendation:

1. identify the requested changes;
2. revise the recommendation;
3. surface any decision that still requires learner input;
4. present the revised recommendation for approval.

A revised curriculum does not become authoritative until explicitly approved.

### If the Curriculum Proposal Itself Must Change

If the Reviewer determines that the Curriculum Proposal itself must be redesigned, the Reviewer does not rewrite it.

The Curriculum Architect owns the Curriculum Proposal.

The Reviewer should state:

> "The proposal requires revision because..."

and return the work to the Curriculum Architect.

The Curriculum Reviewer must not author the Curriculum Proposal.

### Curriculum Changes Follow the Revision Process

Changes to an approved Curriculum Contract are not made by revising this review.

They follow the curriculum revision process:

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
```

For curriculum changes, impact analysis is part of the revision process.

The Reviewer does not independently decide whether impact analysis is necessary.

The Reviewer consumes the results of impact analysis when evaluating a revised curriculum.

---

## 15. Relationship to Other Artifacts

The Curriculum Review:

**Consumes**

* Learning Specification;
* Curriculum Proposal;
* Domain Expert Critique.

**Produces**

* Recommended Curriculum;
* Review Findings;
* Human Decision Points;
* Approval Recommendation.

**Leads to**

* Human Approval;
* Curriculum Contract.

It does not directly produce lessons.

---

## 16. Quality Test

A strong Curriculum Review should allow the learner to understand:

1. What curriculum is being recommended?
2. Why does it serve my goals?
3. What did the Domain Expert identify?
4. Which expert findings were accepted or rejected?
5. What trade-offs were made?
6. What remains uncertain?
7. What decisions do I need to make?
8. What exactly will become authoritative if I approve it?

If the learner cannot answer these questions from the review, the review is not sufficiently clear for approval.

---

## 17. Core Principle

The Reviewer transforms:

> **Expert criticism + curriculum design + learner goals**

into:

> **A coherent curriculum recommendation that the learner can meaningfully approve.**

The Reviewer advises.

**The learner approves.**

