# inspect-runtime

## Purpose
Observe the running system and its environment without changing behavior.

## MUST
- Identify process, endpoint, configuration, logs, and runtime state relevant to the question.
- Capture timestamps and concrete observations where possible.
- Distinguish runtime evidence from source-code expectations.

## MUST NOT
- Restart, mutate, deploy, or alter configuration unless explicitly authorized by a later intervention step.
- Treat logs or metrics without context as complete truth.

## Output
`Observed / Evidence / Expected / Difference / Unknown`
