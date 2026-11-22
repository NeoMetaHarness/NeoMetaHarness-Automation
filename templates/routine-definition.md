# Routine definition — daily readiness digest

## Trigger
On a Neo node at an owner-selected local time. Schedule and timezone are explicit. Never schedule this in GitHub Actions.

## Scope
Read the workspace's approved status events. Produce a private digest of unresolved errors and approvals. Avoid contacting external recipients until the owner configures a destination and grants permission.

## Failure and recovery
Use a stable run ID to avoid duplicate deliveries. Retry transient reads with a limit, record the final failure, and allow an owner to disable the routine.

## Review checklist
Owner, workspace, trigger, inputs, side effects, approval mode, retry limit, output destination, and manual stop are documented before enabling.
