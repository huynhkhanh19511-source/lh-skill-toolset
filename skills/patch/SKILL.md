# patch

## Purpose
Apply a bounded implementation change after the cause and change boundary are understood.

## MUST
- Identify the verified cause or explicitly bounded change requirement.
- Define the smallest safe change.
- Preserve existing invariants unless the decision explicitly changes them.
- List every changed file and why.
- Run targeted verification after mutation.

## MUST NOT
- Silently change architecture or invariants.
- Modify unrelated code.
- Weaken, delete, or bypass tests/validation to obtain a pass.
- Treat passing tests as proof of production correctness.

## Output
`Verified cause/requirement → Change boundary → Files changed → Risk → Verification`
