# Evaluation rubric template

The JSONL cases are synthetic definitions. They have not been executed, and their format is not connected to an evaluator. Replace them with domain tasks and implement checks in the chosen runtime later.

## Required coverage

- Normal work, difficult work and essential missing input.
- Domain accuracy, calculations, attribution and freshness.
- Trusted identity, tenant/project isolation and resource/action boundaries.
- Untrusted retrieved instructions and credential redaction.
- Tool outage, uncertain writes, duplicate prevention and recovery.
- Cancellation, time/cost limits and checkpoint resume.
- Actual destination delivery and truthful completion reporting.

## Scoring

Proposed score per dimension: 0 = failed, 1 = major repair, 2 = minor repair, 3 = meets the defined criterion. Set domain thresholds before release.

| Dimension | Observable check | Weight / threshold |
| --- | --- | --- |
| Domain correctness | Expert reference or deterministic check | TODO |
| Deliverable completeness | Output contract and artifact inspection | TODO |
| Evidence quality | Fresh, attributed evidence supporting claims | TODO |
| Authorized behavior | Runtime/adapter audit and isolation assertions | Critical failures: zero |
| Recovery reliability | Timeout, retry, cancellation and resume scenarios | TODO |
| Efficiency | Measured time, token use and cost | TODO |
| Delivery | Destination receipt or readback | TODO |

## Release criteria

- Every required case is executed with reproducible inputs and recorded results.
- Critical failures are zero; quality thresholds are filled and met.
- The actual runtime, model, tools, credentials and host are exercised through a complete task.
- Permission enforcement is tested in the runtime and adapters beyond prompt behavior.
- The named owner reviews domain quality where the output contract requires it.

## Result record

- Evaluation ID / date / owner: TODO
- Harness, prompt, rules, configuration and fixture versions: TODO
- Runtime, model and tool versions: TODO
- Case results and evidence locations: TODO
- Time, usage and cost: TODO
- Failed cases, fixes and rerun evidence: TODO
- Release decision and unresolved limitations: TODO
