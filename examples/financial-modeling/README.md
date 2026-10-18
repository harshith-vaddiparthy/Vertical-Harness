# Financial Modeling Harness

A standalone financial-modeling specialization built from this Vertical Harness template and two MIT-licensed skills: startup-financial-modeling from wshobson/agents and financial-modeling from Claude Office Skills.

Repository: [Financial-Modeling-Harness](https://github.com/harshith-vaddiparthy/Financial-Modeling-Harness).

It implements five revenue models, role-based hiring, linked monthly income statements/balance sheets/cash flow, working capital, debt and priced equity rounds, scenarios, sensitivity recalculation and auditable private run records. A native skill and six stdio MCP tools connect it to Hermes without replacing the agent's existing inference provider.

```bash
git clone https://github.com/harshith-vaddiparthy/Financial-Modeling-Harness.git
cd Financial-Modeling-Harness
python3 -m harness doctor
python3 -m harness run examples/saas.json
```

Requires Python 3.10+. Open the returned HTML report, then verify its run ID with `python3 -m harness verify RUN_ID`. Original synthetic examples, JSON/CSV exports, a portable interactive report, financial-invariant tests and Hermes setup instructions live in the standalone repository. Cash deficits remain visible rather than being hidden by a funding plug. CSVs are saved snapshots; editable Excel workbooks and complex accounting/capital structures require extensions.

The implementation and vendored upstream skills stay in the standalone repository. This parent repository remains the reusable harness template.
