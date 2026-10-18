# Primary workflow template

- Workflow name: TODO
- Trigger: TODO
- Intended result: TODO
- Run owner and delivery destination: TODO

## Lifecycle

Proposed states: `received → validated → running → verifying → delivering → completed`.
Additional states: `awaiting_input`, `incomplete`, `failed`, `cancelled`. Persist the last completed step, side effects and resume target before transitioning.

| Step | Action | Completion criterion | Failure handling |
| --- | --- | --- | --- |
| Intake | Record request, trusted identity, tenant/project, input and destination. | Required inputs and authorized scope are identified. | Ask only for essential missing facts; retain state. |
| Validate | Check configuration, resource grants, source freshness and tools. | Intended actions have valid authority and usable prerequisites. | Report the exact unresolved prerequisite. |
| Plan | Select domain procedure, tools and bounded time/cost allocation. | Steps, side effects and success checks are explicit. | Resolve scope-changing uncertainty before dependent actions. |
| Execute | Apply domain rules; authorize each action; checkpoint results. | Each planned action has a recorded result or known unresolved state. | Use bounded transient retries; inspect state before retrying writes. |
| Verify | Evaluate against the output contract and inspect affected resources. | Every acceptance criterion has passing evidence. | Repair within scope and budget; otherwise report incomplete. |
| Deliver | Deliver to the authorized destination using a supported adapter. | Receipt or destination readback is observed. | Reconcile uncertain delivery before another send. |
| Close | Save the run record and report result and evidence. | Final status matches the observed outcome. | Preserve pending work and a precise resume point. |

## Specialize the execution step

1. TODO: Domain input preparation.
2. TODO: Specialist analysis or action.
3. TODO: Domain verification.

## Recovery and cancellation

- Idempotency key and external status lookup: TODO
- Checkpoint backend and resume procedure: TODO
- Cancellation mechanism and side effects already committed: TODO
- Compensating action / rollback owner: TODO
- Human escalation destination when required: TODO

Use [the run record](../templates/run-record.md) for actual runs. Budget exhaustion preserves a checkpoint and produces an incomplete status.
