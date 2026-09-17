# LH Skill Toolset

> **Skills = nouns. Primitives = verbs. Agent = executor.**

An evidence-first skill contract library for Forward Deployed Engineering (FDE).

The goal is not to make agents *more autonomous*.
The goal is to make agent execution **bounded, observable, and evidence-driven**.

## Operating Loop

```text
Reality
  ↓
Understand
  ↓
Investigate
  ↓
Verify
  ↓
Implement
  ↓
Own Outcome
```

Core principle:

> **Abstraction cannot escape Runtime.**

A skill is useful only when its contract survives contact with a real, unfamiliar system.

## Skill Model

```text
                 LH
          Architecture / Decision
                    │
                    ▼
             Skill Toolset
          ┌─────────┴─────────┐
          │                   │
       Skills              Workflows
      (nouns)             (composition)
          │                   │
          ▼                   ▼
      Primitives ────────→ Agent
       (verbs)            (executor)
```

Skills define **what capability is being exercised**.
Primitives define **what action is performed**.
The agent executes them against Runtime Reality.

## Taxonomy

### Reality

Establish what actually exists before changing it.

- `repo-map` — map an unfamiliar repository
- `trace-flow` — trace concrete behavior and state transitions
- `inspect-runtime` — observe the running system and environment

### Investigation

Turn failures and unknowns into explicit, testable claims.

- `reproduce` — make an observed failure repeatable
- `hypothesize` — construct explicit hypotheses and falsifiers
- `verify` — confirm or reject a claim with evidence

### Intervention

Make bounded changes and verify their immediate behavior.

- `patch` — apply the smallest justified change
- `test` — execute verification against behavior/invariants
- `deploy` — move a verified change to a target runtime

### Ownership

Establish whether the change actually achieved the intended outcome.

- `validate` — validate behavior in the target runtime
- `document` — persist reality, evidence, decisions, and unknowns

## Workflows

Skills compose into explicit operating workflows:

```text
onboard
repo-map → trace-flow → inspect-runtime → document


debug
repo-map → trace-flow → reproduce → hypothesize → verify → patch → test


change
repo-map → trace-flow → verify → patch → test → validate → document
```

The workflow is a sequence of **evidence gates**, not merely a checklist.

## Core Invariants

1. **Evidence before mutation.**
2. **Read-only Reality before intervention.**
3. **A hypothesis is not a fact.**
4. **An agent must not silently change architecture or invariants to make a test pass.**
5. **Passing tests does not establish production correctness.**
6. **Unknown remains Unknown until verified.**
7. **Failed or rejected hypotheses remain evidence.**

## Evidence Format

The default evidence language is:

```text
Observed
  ↓
Evidence
  ↓
Inference
  ↓
Hypothesis
  ↓
Verification
  ↓
Decision
  ↓
Intervention
  ↓
Outcome
  ↓
Unknowns
```

This keeps **Reality**, **Inference**, and **Decision** separate.

## V0 Scope

V0 establishes the minimum contract library and workflow composition needed to exercise the toolset against a real unfamiliar repository.

First reality target:

`inventory-reality-lab`

V0 is successful when the toolset can onboard and investigate a real repo without hiding uncertainty or jumping directly into mutation.

## Repository Structure

```text
lh-skill-toolset/
├── README.md
├── skills/
│   ├── repo-map/
│   ├── trace-flow/
│   ├── inspect-runtime/
│   ├── reproduce/
│   ├── hypothesize/
│   ├── verify/
│   ├── patch/
│   ├── test/
│   ├── deploy/
│   ├── validate/
│   └── document/
└── workflows/
    ├── onboard.md
    ├── debug.md
    └── change.md
```

## Design Rule

> **Do not abstract away a failure before understanding it.**

Failures encountered while exercising the toolset against Runtime Reality become evidence for the next version of the toolset.

That is how the contracts evolve: **Reality → Evidence → Refinement.**
