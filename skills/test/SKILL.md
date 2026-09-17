# test

## Purpose
Execute or create verification that checks an explicit behavior or invariant.

## MUST
- State what behavior is being verified.
- Prefer focused tests that cover the changed or failed path.
- Report pass/fail and relevant output.
- Include negative and boundary cases when they protect an important invariant.

## MUST NOT
- Rewrite expectations merely to make the test pass.
- Remove failing tests without explaining the behavioral decision.
- Equate test success with deployment success.

## Output
`Target → Test → Expected → Actual → Status → Evidence`
