# Operations runbook template

Status: design document. Commands and infrastructure have not been selected.

## Runtime readiness

| Requirement | Selected value / evidence |
| --- | --- |
| Execution host, environment and identity | TODO |
| Runtime, installation and version pin | TODO |
| Config loader, schema validation and unresolved-field checks | TODO |
| Authentication and authorization enforcement | TODO |
| Model route and full consumer test | TODO |
| Tool adapters and credential references | TODO |
| Scope isolation and context retrieval | TODO |
| Durable task state and idempotency | TODO |
| Artifact storage, logs and backups | TODO |
| Cancellation, limits and health checks | TODO |
| Evaluations and first completed task | TODO |

## Start and inspect

1. Verify the intended host, environment, identity and loaded configuration.
2. Validate required fields and credential availability without exposing secret values.
3. Run the selected start command: TODO.
4. Inspect the health check and actual runtime model/tool path: TODO.
5. Run a scoped representative task and verify its artifact and destination receipt.

## Failures

| Symptom | First inspection | Recovery | Completion evidence |
| --- | --- | --- | --- |
| Model request fails | Actual consumer, endpoint, deployment and error class | Bounded retry or configured compatible fallback | Real runtime task succeeds |
| Tool returns unauthorized | Requester, scope, service identity and credential grants | Correct only the defective authorized mapping | Permitted action succeeds; denied scope remains denied |
| Write outcome unknown | External operation ID / idempotency status | Reconcile original action before replay | Single verified side effect |
| Run interrupted | Last checkpoint and committed actions | Resume from verified state | No duplicated side effects |
| Context is stale | Source timestamp and authority rule | Refresh within authorized source scope | Updated attributed evidence |
| Budget exhausted | Usage and checkpoint | Report incomplete and use an authorized new budget | Completed run stays within allocation |

## Logs and monitoring

- Record run ID, trusted identity/scope, versions, step, tool operation IDs and status.
- Capture model usage, latency, cost and verification evidence.
- Redact secrets and unnecessary personal data; configure retention and scoped access.
- Health signal, alert destination and operational owner: TODO.

## Stop, rollback and restore

- Stop / cancel command and expected state: TODO
- Configuration or runtime rollback reference: TODO
- External side effects requiring reconciliation: TODO
- Backup and restore procedure: TODO
- Restore verification and owner: TODO
