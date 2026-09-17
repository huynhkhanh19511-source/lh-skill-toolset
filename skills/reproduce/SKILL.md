# reproduce

## Purpose
Turn a reported failure into a repeatable observation.

## MUST
- Capture the exact trigger, inputs, environment, and observed result.
- Reproduce before proposing a fix when reproduction is feasible.
- Record whether reproduction is deterministic, intermittent, or unknown.

## MUST NOT
- Change production behavior to make reproduction easier without authorization.
- Claim a bug is fixed because reproduction stopped without verification.

## Output
`Trigger / Environment / Steps / Expected / Actual / Reproducibility / Evidence`
