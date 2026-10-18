# Vertical Harness

An open-source starting template for designing a specialized AI agent harness: the instructions, domain knowledge, model configuration, tools, access rules and workflows that let an agent do one specific job reliably.

Use it for a focused vertical such as finance operations, course production or customer support. Define what the specialist does, where tasks run, who has access and what evidence proves a task is finished.

**Current status:** a planning and configuration template. It contains no runtime implementation or connected services. The example configuration format must be adapted and enforced by the runtime you choose.

## Fork and get started

1. Click **Fork** on this repository to create your own copy, or use **Use this template** to start a fresh repository.
2. Clone your copy:

   ```bash
   git clone https://github.com/YOUR-USERNAME/Vertical-Harness.git
   cd Vertical-Harness
   ```

   If you chose a different repository name, use that name in the commands.

3. Start with [task.md](task.md): name your vertical, describe one specialist job and define a representative task.
4. Fill `config/` with your execution host, user/team access, model, tools and context sources. Add domain rules in `domain/` and tailor [the primary workflow](workflows/primary.md).
5. Replace [the synthetic evaluation cases](evals/cases.example.jsonl) with real examples from your vertical. Then implement the harness using your chosen runtime and verify a complete task.

No installation is needed to fill in the template. `TODO` and `null` mark undecided values. Keep `.example` files as design references until your runtime defines validated operational configuration.

## What's included

```text
task.md       Starting brief and decisions to fill in
AGENTS.md     Instructions for agents working with the template
config/       Host, access, model, tools, context and execution limits
domain/       Specialist scope, vocabulary, rules and output contract
workflows/    Task lifecycle, verification and recovery
prompts/      Specialist system prompt template
evals/        Example cases and quality rubric
operations/   Readiness, monitoring, recovery and rollback
templates/    Run evidence and design decision records
```

Keep credentials outside the repository and reference your execution host's secret manager. Access rules and prompts describe intended behavior; your runtime and tool adapters must enforce permissions, isolation and budgets.

## Examples

Explore [specialized harness examples](examples/README.md). [Android TV Harness](examples/android-tv/README.md) is a separate executable Android TV/Google TV specialization with one optional @J.A.R.V.I.S. button, verified device actions and recovery. Its implementation lives in [Android-TV-Harness](https://github.com/harshith-vaddiparthy/Android-TV-Harness); this repository remains the reusable template.

## License

[MIT](LICENSE). You can fork, modify and use this template, including commercially, under the license terms.
