# validate

## Purpose
Check behavior after deployment or change against the intended outcome and important invariants.

## MUST
- Validate the real target runtime when possible.
- Check the user/customer-visible behavior, not only internal tests.
- Compare observed behavior with expected behavior.
- Record residual risk and unknowns.

## MUST NOT
- Declare production correctness from CI alone.
- Ignore environment-specific failures.
- Turn unknowns into success claims.

## Output
`Target → Expected outcome → Observed outcome → Invariants → Evidence → Residual risk`
