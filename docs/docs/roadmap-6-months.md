# 6-month roadmap: become a reliable agent operator

## Target state

By month 6, produce two auditable proofs:

1. A reproducible benchmark or evaluation harness with public methodology, results and failure analysis.
2. A production workflow with real users, a measured baseline and a clear human escalation path.

The goal is not to use the largest number of agents. It is to increase delegated work without increasing risk and rework at the same rate.

## Learn

### Evaluation engineering

- Build gold sets from real tasks and explicit rubrics.
- Separate component, trajectory and business-outcome metrics.
- Measure calibration, abstention and escalation.
- Use adversarial cases and distribution slices, not one aggregate score.
- Version model, prompt, tool schema, environment and evaluator.
- Compare against a no-agent or human baseline.

### Production semantics

- Idempotency, retries, timeouts and dead-letter handling.
- Concurrency, stale state, locks and backpressure.
- SLOs, cost budgets, tracing and replay.
- Canary releases, rollback and provider failure modes.

### Agent security

- Threat modeling and prompt-injection boundaries.
- Least privilege per tool and task.
- Sandboxing and secret handling.
- Approval gates for irreversible, expensive or external actions.
- Static, dynamic and dependency analysis.

### Verification

- Property-based and fuzz testing.
- Contract tests around integrations.
- Metamorphic tests where exact answers vary.
- Incident-derived regression suites.

## Build

### Project A: a finished benchmark

Minimum bar:

- public task contract and versioned manifest;
- deterministic environment where possible;
- multiple scenarios and seeds;
- fixed budgets across models;
- mean, dispersion, worst case, completion and cost;
- persistent execution traces and replays;
- failure atlas with examples;
- hosted or one-command reproduction.

A benchmark without an oracle and failure analysis is a demo.

### Project B: one vertical workflow

Choose a domain where access and judgment already exist. The workflow needs:

- 3-5 design users;
- a task repeated at least weekly;
- baseline time, quality and error cost;
- real permissions and data;
- a verifiable output or decision;
- human escalation proportional to risk;
- four weeks of observed use.

Prefer a narrow decision or workflow over a generic knowledge platform or agent platform.

## Avoid

- Opening another repository before one reaches users and measurement.
- Learning frameworks only to list them.
- Multi-agent topology without an A/B comparison against a simple loop.
- A benchmark with one model, one prompt or one seed.
- Counting tokens, commits or generated lines as impact.
- Hiding manual operations required to keep the system working.

## Six-month sequence

### Weeks 1-2

- Define personal baseline metrics.
- Select the benchmark and one vertical workflow.
- Write acceptance criteria and kill criteria before implementation.

### Weeks 3-8

- Close the benchmark contract, oracle and replay path.
- Run first controlled model comparisons.
- Recruit design users and shadow the existing workflow.

### Weeks 9-16

- Deploy the narrowest usable vertical.
- Add tracing, security boundaries and escalation.
- Collect failures and turn them into a versioned eval set.

### Weeks 17-24

- Publish benchmark results and failure atlas.
- Measure retention and workflow impact.
- Remove complexity not justified by data.
- Write one technical report focused on a hard decision and evidence.

## Exit criteria

- Another engineer can reproduce benchmark results from the documentation.
- At least two comparable agent/model evaluations are complete.
- At least 30 failures are classified, with important ones covered by regressions.
- Three to five real users try the workflow; at least two use it for four consecutive weeks.
- A task-level outcome improves by roughly 30% or more without breaching the chosen risk budget.
- Routine changes are mostly delegated, while reopened or reverted changes stay below 10%.
- The project has an explicit decision: continue, narrow, pivot or stop.
