# reproduce

## Purpose
Turn a reported failure into a repeatable observation.

## MUST
- Capture the exact trigger, inputs, environment, and observed result.
- Reproduce before proposing a fix when reproduction is feasible.
- Record whether reproduction is deterministic, intermittent, or unknown.
- Declare any mutation before executing it.
- Capture relevant pre-state before a mutation.
- Record every mutation performed and its effect.
- Preserve or restore state when safe and feasible, and explicitly report restoration.

## MUST NOT
- Change production behavior to make reproduction easier without explicit authorization.
- Silently mutate persistent state.
- Silently reset, seed, or restore data.
- Claim an experiment was read-only when it was not.
- Claim a bug is fixed because reproduction stopped without verification.

## Mutation Protocol
Before a mutating experiment, state:

`Mutation / Target / Reason / Pre-state / Expected effect`

After execution, record:

`Actual effect / Post-state / Restoration / Evidence`

## Output
`Trigger / Environment / Steps / Expected / Actual / Reproducibility / Mutation / Evidence`
