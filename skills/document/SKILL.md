# document

## Purpose
Persist system reality, decisions, changes, and evidence so future work starts from known context.

## MUST
- Record facts separately from inference and decisions.
- Link claims to concrete evidence.
- Capture important invariants, changes, and unresolved unknowns.
- Make the record understandable without hidden conversation context.
- Distinguish repository evidence from assumptions about product intent.
- Label product-intent or architectural characterization as inference unless explicitly documented by the system owner.
- Record the scope and enforcement point of important invariants.

## MUST NOT
- Rewrite history to make the outcome look cleaner.
- Record assumptions as facts.
- Treat inferred product intent as documented requirement.
- State an invariant without identifying where it applies and where it is enforced when that distinction matters.
- Omit important failed or rejected hypotheses.

## Invariant Record
For important invariants, capture:

`Invariant / Scope / Enforcement Point / Evidence / Known Exceptions or Uncovered Paths`

## Output
`Reality → Evidence → Decision → Change → Verification → Outcome → Unknowns`
