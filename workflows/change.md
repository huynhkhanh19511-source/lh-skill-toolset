# change

## Goal
Make a bounded change while preserving ownership of architecture and outcome.

## Sequence
`repo-map → trace-flow → verify → patch → test → validate → document`

## Gate
The agent may implement the bounded intervention, but must not silently change architecture, invariants, or success criteria. Production validation is a separate step.