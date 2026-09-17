# verify

## Purpose
Seek evidence that confirms or rejects a specific hypothesis or claimed behavior.

## MUST
- Define the claim being tested.
- Use the strongest available evidence: runtime behavior, targeted test, trace, data, or source inspection.
- State Confirmed, Rejected, or Inconclusive.
- Preserve contradictory evidence.

## MUST NOT
- Treat correlation as confirmation.
- Change the hypothesis silently.
- Declare success from an unrelated passing check.

## Output
`Claim → Test/Evidence → Result → Confidence → Remaining Unknowns`
