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
- For every material boundary, classify it and record:
  - boundary type
  - source
  - destination
  - input
  - transformation
  - output
  - governing contract / invariant
  - validation / enforcement point
  - failure mode
  - evidence
- A boundary is material when crossing it can change state, representation, authority, dependency, contract, or semantic meaning.
- Do not require classification for every internal function call; only record material boundaries.
- Multiple boundary types may apply to a single boundary when justified.
- Allowed boundary types: state, data, external_dependency, semantic, api, persistence.
- If the governing contract is unknown, report `Unknown`.

## MUST NOT
- Speculate architecture without evidence.
- Modify code while investigating.
- Stop at the first plausible function.
- Generalize an invariant beyond the execution path where it is actually enforced.
- Invent contracts or invariants that are not evidenced in the runtime or code.

## Procedure
1. Identify trigger.
2. Follow calls.
3. Identify reads/writes and state transitions.
4. Locate material boundaries that change state, representation, authority, dependency, contract, or semantic meaning.
5. For each material boundary, capture:
   1. boundary type
   2. source
   3. destination
   4. input
   5. transformation
   6. output
   7. governing contract / invariant
   8. validation / enforcement point
   9. failure mode
   10. evidence
6. Locate external side effects.
7. Locate validation/enforcement points.
8. Check whether the same invariant is enforced on alternate paths such as replay, recovery, reads, or imports.
9. Record evidence and gaps.

## Evidence Format
`Trigger → Call chain → Material boundary → boundary type → source → destination → input → transformation → output → governing contract/invariant → validation point → failure mode → evidence → Unknown`

## Boundary Example
`API request → app handler → state projection → persistence boundary (api + state + persistence) → current stock derived from replay → invariant enforcement on write path → evidence → Unknown`
