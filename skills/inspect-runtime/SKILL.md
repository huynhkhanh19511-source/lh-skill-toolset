# inspect-runtime

## Purpose
Observe the running system and its environment without changing behavior or persistent state.

## MUST
- Identify process, endpoint, configuration, logs, and runtime state relevant to the question.
- Capture timestamps and concrete observations where possible.
- Distinguish runtime evidence from source-code expectations.
- Operate read-only during inspection.
- If a mutation is required to answer the question, stop inspection and hand off to `reproduce` or another explicitly authorized intervention step.

## MUST NOT
- Write files or modify persistent data.
- POST, PUT, PATCH, or DELETE application state.
- Restart, stop, or alter processes.
- Alter configuration.
- Reset, seed, or restore application/test data.
- Treat logs or metrics without context as complete truth.

## Mutation Boundary
`inspect-runtime` is strictly read-only.

Runtime experiments such as sending mutating requests, changing files, restarting processes, or resetting state belong to `reproduce`/`verify` and must be explicitly declared as mutations before execution.

## Output
`Observed / Evidence / Expected / Difference / Unknown`
