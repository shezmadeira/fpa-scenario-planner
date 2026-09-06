# FP&A Scenario Planner

Internal planning application for forecasting ARR and revenue using Athena actuals and user-entered New, Expansion, Contraction, and Churn assumptions. Intended hosting: Fly.io.

## Status

Architecture and scope only. Application implementation and deployment have not started.

## Initial scope

- Monthly forecasts over 24–36 months, with configurable fiscal years.
- Enterprise and Self-Serve assumptions, with material customer overrides.
- Base, Upside, and Downside scenarios.
- Monthly dollar and percentage assumptions with explicit denominators.
- Separate revenue timing and usage/non-recurring revenue assumptions.
- Versioned actuals snapshots, scenario history, and CSV export.
- Company authentication with viewer, editor, and approver roles.

See [architecture](docs/architecture.md) for the proposed design and decisions to settle before implementation.

## Suggested implementation structure

```text
frontend/       React and TypeScript planning interface
backend/        API, Athena refresh worker, persistence
model/          Deterministic forecast calculations
tests/          Financial reconciliation and integration tests
docs/           Architecture and metric definitions
```

These implementation directories will be introduced as development begins.
