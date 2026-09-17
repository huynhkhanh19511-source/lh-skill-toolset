# trace-flow

## Purpose
Trace a concrete behavior from entry point to logic, state transition, and side effect.

## MUST
- Start from a real entry point.
- Trace Request → Logic → State → Side Effect.
- Identify the state transition and persistence boundary.
- Show evidence from code or runtime.
- When tracing an invariant, identify its scope and enforcement point.
- Distinguish enforcement on new writes/events from behavior during historical replay or read-time reconstruction.

## MUST NOT
- Speculate architecture without evidence.
- Modify code while investigating.
- Stop at the first plausible function.
- Generalize an invariant beyond the execution path where it is actually enforced.

## Procedure
1. Identify trigger.
2. Follow calls.
3. Identify reads/writes and state transitions.
4. Locate external side effects.
5. Locate validation/enforcement points.
6. Check whether the same invariant is enforced on alternate paths such as replay, recovery, reads, or imports.
7. Record evidence and gaps.

## Evidence Format
`Trigger → Call chain → State transition → Side effect → Enforcement point → Scope → Evidence → Unknown`
