# Agent instructions for this template

## Current scope

This folder is a vertical harness template. Template work includes documents, example configuration and evaluation definitions. Runtime implementation begins when the user requests it; preserve unresolved fields until decisions are supplied or safely inferred from that request.

## Reading order

1. Read `task.md` for the specialist job, current request and missing decisions.
2. Read `domain/brief.md` and `domain/rules.md` when defining specialist behavior.
3. For execution placement, read `config/deployment.example.yaml`. For identities or permissions, read `config/access.example.yaml`. For model routing, read `config/models.example.yaml`.
4. Before defining tool actions or retrieval, read `config/tools.example.yaml` and `config/context.example.yaml`.
5. For task flow and completion, read `workflows/primary.md` and `domain/output-contract.md`. For quality review, read `evals/rubric.md` and relevant cases.
6. For deployment or recovery, read `operations/runbook.md`.

## Editing and evidence

- Keep detailed policy in its owning file and reference it elsewhere.
- Label proposed limits and synthetic examples. Record undecided values as `TODO` or `null`.
- Preserve unrelated work, existing host credentials and global model configuration.
- Store credential references in examples; keep secret values outside this template.
- Validate syntax and local references after template changes.
- Describe requirements still unimplemented. Permission prose and prompts do not establish runtime enforcement.
- For actual task runs, use `templates/run-record.md`; support completion claims with direct evidence.
