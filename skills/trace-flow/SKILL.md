# trace-flow

## Purpose
Trace a concrete behavior from entry point to logic, state transition, and side effect.

## MUST
- Start from a real entry point.
- Trace Request → Logic → State → Side Effect.
- Identify the state transition and persistence boundary.
- Show evidence from code or runtime.

## MUST NOT
- Speculate architecture without evidence.
- Modify code while investigating.
- Stop at the first plausible function.

## Procedure
1. Identify trigger.
2. Follow calls.
3. Identify reads/writes and state transitions.
4. Locate external side effects.
5. Record evidence and gaps.

## Evidence Format
`Trigger → Call chain → State transition → Side effect → Evidence → Unknown`
