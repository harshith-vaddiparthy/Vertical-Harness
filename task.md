# Vertical harness — starting brief

Status: template only. Fill in this file first. `TODO` and `null` mean undecided.

## Outcome

- Harness name: TODO
- Vertical / domain: TODO
- Specialist job in one sentence: TODO
- Primary user and problem: TODO
- Accountable owner: TODO
- Successful finished deliverable: TODO
- Work explicitly outside this harness: TODO

## Decisions to provide

| Decision | Your answer | Detailed template |
| --- | --- | --- |
| Where tasks execute: host, runtime, workspace | TODO | [Deployment](config/deployment.example.yaml) |
| Who uses it: just me, team, or customers | TODO | [Access](config/access.example.yaml) |
| What each person may read, change, or approve | TODO | [Access](config/access.example.yaml) |
| Provider, model, reasoning, context and cost limits | TODO | [Models](config/models.example.yaml) |
| Tools, accounts, resources and allowed actions | TODO | [Tools](config/tools.example.yaml) |
| Domain sources and allowed memory | TODO | [Context](config/context.example.yaml) |
| Task trigger and delivery destination | TODO | [Workflow](workflows/primary.md) |
| Domain rules and unacceptable mistakes | TODO | [Rules](domain/rules.md) |
| Definition of done and quality threshold | TODO | [Output contract](domain/output-contract.md), [Evaluations](evals/rubric.md) |

## First representative task

- Input / request: TODO
- Trusted requester identity: TODO
- Account / project / tenant: TODO
- Desired output and destination: TODO
- Time and cost limit: TODO
- Allowed side effects: TODO
- Evidence that proves completion: TODO
- Missing facts that must be resolved: TODO

## Template completion checklist

- [ ] Describe one narrow specialist job in [the domain brief](domain/brief.md).
- [ ] Fill execution, access, model, tool and context decisions.
- [ ] Specify one primary workflow and its finished deliverable.
- [ ] Replace evaluation examples with realistic tasks and failure cases.
- [ ] Record unresolved architecture choices in [a decision record](templates/decision.md).

## Later implementation checklist

These are future build requirements, not completed work.

- [ ] Select the runtime and implement validated configuration loading.
- [ ] Enforce identity, resource permissions and tool policies in code.
- [ ] Implement task state, recovery, budgets and artifact storage.
- [ ] Run representative evaluations and inspect delivered outputs.
- [ ] Verify the whole path on the selected host and delivery surface.

Template completion and an operational harness are separate milestones.
