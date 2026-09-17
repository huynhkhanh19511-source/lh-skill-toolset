# repo-map

## Purpose
Establish a factual map of an unfamiliar repository before deeper investigation or mutation.

## Input
Repository path and optional scope.

## Output
Entry points, modules, data stores, external dependencies, execution paths, tests, and explicit unknowns.

## MUST
- Inspect the actual repository structure and relevant files.
- Identify executable entry points and important boundaries.
- Cite concrete file paths and symbols as evidence.
- Separate Observed, Inference, and Unknown.

## MUST NOT
- Invent architecture not supported by repository evidence.
- Modify files during mapping.
- Treat filenames alone as proof of runtime behavior.

## Procedure
1. Inventory structure.
2. Locate entry points.
3. Trace major boundaries.
4. Identify state stores and tests.
5. Record evidence and unknowns.

## Evidence Format
`Observed → Evidence(path/symbol) → Inference → Unknown`
