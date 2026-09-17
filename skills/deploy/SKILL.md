# deploy

## Purpose
Move a verified change into a target runtime environment through an explicit deployment path.

## MUST
- Confirm the change and required tests are verified before deployment.
- Identify target environment and deployment mechanism.
- Record deployment result, version/commit, and runtime evidence.
- Define rollback or recovery path when applicable.

## MUST NOT
- Deploy an unverified change by default.
- Claim production success from build success alone.
- Hide deployment failures.

## Output
`Artifact/Commit → Target → Deployment action → Runtime result → Rollback state`
