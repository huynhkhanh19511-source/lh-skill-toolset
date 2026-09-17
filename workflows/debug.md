# debug

## Goal
Investigate a failure without guessing into a patch.

## Sequence
`repo-map → trace-flow → reproduce → hypothesize → verify → patch → test`

## Gate
No patch before a sufficiently verified cause. Every hypothesis must have supporting evidence and a falsifier. Failed verification remains evidence.