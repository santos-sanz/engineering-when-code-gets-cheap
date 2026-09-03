# Engineering when code gets cheap

A practical roadmap for becoming a stronger engineer or technical founder as coding agents improve.

The premise is deliberately narrow: frontier agents keep getting better at well-scoped implementation tasks over the next three years. This repository asks what to learn, build, stop doing, and measure if that premise is roughly right.

It does **not** assume that agents become reliable autonomous engineers on a fixed date. Current evidence shows rapid capability growth and real productivity gains, but also large gaps between benchmarks and messy production work. The plan is designed to work under both fast and slower progress.

## The core thesis

> Do not compete with an agent on typing code. Compete on turning ambiguous problems into reliable systems that produce a measurable result.

Implementation is losing scarcity faster than responsibility. As code gets cheaper, value moves toward:

- choosing the right problem;
- expressing constraints and invariants;
- building evaluation and verification loops;
- integrating with real data, permissions and workflows;
- operating failures safely;
- earning distribution and trust;
- owning an economic outcome.

## Repository map

| Document | Question it answers |
|---|---|
| [State of coding agents](docs/state-of-coding-agents.md) | What does the evidence actually show in 2026? |
| [Skills matrix](docs/skills-matrix.md) | Which skills rise, fall, or change shape? |
| [6-month roadmap](docs/roadmap-6-months.md) | How do I become a reliable operator of coding agents? |
| [15-month roadmap](docs/roadmap-15-months.md) | How do I own an end-to-end technical outcome? |
| [36-month roadmap](docs/roadmap-36-months.md) | What durable moat can an engineer or founder build? |
| [Measurement system](docs/measurement.md) | How do I know whether I am improving? |
| [Reading list](docs/reading-list.md) | Which primary sources are worth revisiting? |

## What a senior engineer does when code is cheap

A senior engineer increasingly designs the **system that produces changes**, rather than being its fastest code author:

1. Select the problem and define a result that counts.
2. Reduce the solution space with contracts, invariants and budgets.
3. Split work into units an agent can execute and verify independently.
4. Build the evaluation environment before scaling generation.
5. Decide which properties can be checked automatically and which need a human.
6. Integrate changes with existing systems, data, permissions and people.
7. Operate incidents and turn every important failure into a regression test.
8. Stop low-value work even when generating it is almost free.

The target is not maximum agent activity. It is maximum **validated value per hour of human attention**, subject to explicit limits on cost, defects and risk.

## Roadmap at a glance

| Horizon | Target state | Proof |
|---|---|---|
| 6 months | Reliable agent operator | Reproducible benchmark plus one real workflow with users and baselines |
| 15 months | Owner of an outcome | Production case with adoption, economics, SLOs and a controlled model migration |
| 36 months | Builder of durable assets | Domain, proprietary feedback, distribution, trust and operational track record |

## Operating principles

- Prefer one finished, measured system over four impressive demos.
- Treat every benchmark as a model of reality, not reality itself.
- Make the verifier stronger before making the generator busier.
- Use agents to shorten the loop from hypothesis to evidence, not to multiply features.
- Keep architecture as simple as the measured task permits.
- Measure outcomes and defects, not lines of code, prompts or agent count.
- Learn frameworks when a task needs them. Invest deeply in concepts that survive frameworks.

## Evidence standard

Claims in this repository favor primary sources: benchmark maintainers, field experiments, large usage studies and peer-reviewed security research. Vendor studies are useful but labeled by context and should not be treated as neutral labor-market forecasts. See [the state-of-the-art review](docs/state-of-coding-agents.md) and [reading list](docs/reading-list.md).
