# State of coding agents in 2026

## Executive view

Four observations can be defended from current evidence:

1. **The size of well-specified tasks agents can complete is growing quickly.**
2. **Benchmark time horizon is not the same thing as unattended real-world autonomy.**
3. **Productivity gains are real for selected work, but speed gains exceed value gains.**
4. **Domain expertise, verification and organizational quality remain force multipliers.**

That is enough to plan for much cheaper implementation. It is not enough to forecast a date when software engineers disappear.

## Capability: the delegable unit is getting larger

METR defines a task-completion time horizon as the human-expert duration of tasks at which an agent reaches a specified probability of success. Its current suite contains software engineering, ML and cybersecurity work with clear grading. METR reported roughly 6x growth over nine months and expanded its TH 1.1 suite to 228 tasks.

This is strong evidence that the unit of work one can delegate is growing. It is easy to misread:

- A 50% horizon is not acceptable for reliability-critical work.
- It measures task difficulty in expert-human time, not how long an agent runs unattended.
- The suite favors self-contained, well-defined and automatically gradable tasks.
- Performance varies by orders of magnitude across domains.
- METR warns that its current estimates above 16 hours are unreliable.

**Engineering implication:** the valuable skill is converting messy work into bounded tasks with machine-checkable completion conditions.

Sources:

- METR, [Task-Completion Time Horizons of Frontier AI Models](https://metr.org/time-horizons/)
- METR, [Clarifying limitations of time horizon](https://metr.org/notes/2026-01-22-time-horizon-limitations/), 2026-01-22
- METR, [Time Horizon 1.1](https://metr.org/blog/2026-1-29-time-horizon-1-1/), 2026-01-29

## Productivity: distinguish speed, output and value

The widely cited METR randomized trial found that experienced open-source developers using early-2025 tools took 19% longer. METR now calls that result out of date. A later trial showed signs of acceleration, but selection effects made the magnitude unreliable: developers increasingly declined to work without AI.

Two 2026 studies illustrate why claims need careful wording:

- In a survey of 349 technical workers, the median self-reported change was 1.4-2x in value and 3x in speed. METR warns that perceptions tend to overstate causal productivity.
- An analysis of 5,305 Claude Code transcripts from seven METR staff estimated 1.5-13x time savings on the selected agent-assisted tasks. The authors call this a soft upper bound, not an overall productivity multiplier, because people select suitable tasks and may use saved time for lower-value work.

DORA's 2025 result is a useful organizational frame: AI amplifies the system in which it is deployed. Fast generation magnifies good feedback and platform practices, but also weak ownership and quality controls.

**Engineering implication:** measure time to a validated outcome, cost per correct result, defect escape rate and adoption. Do not use generated lines, commits or closed tickets as the headline.

Sources:

- METR, [We are Changing our Developer Productivity Experiment Design](https://metr.org/blog/2026-02-24-uplift-update/), 2026-02-24
- METR, [Measuring the Self-Reported Impact of Early-2026 AI on Technical Worker Productivity](https://metr.org/blog/2026-05-11-ai-usage-survey/), 2026-05-11
- METR, [Analyzing coding agent transcripts to upper bound productivity gains](https://metr.org/notes/2026-02-17-exploratory-transcript-analysis-for-estimating-time-savings-from-coding-agents/), 2026-02-17
- Google DORA, [State of AI-assisted Software Development 2025](https://dora.dev/research/2025/dora-report/)

## Adoption: implementation work is moving toward automation

Anthropic analyzed 500,000 coding interactions in 2025. It classified 79% of Claude Code conversations as automation, compared with 49% on Claude.ai. UI, UX and common web-development tasks were prominent; startups appeared as earlier adopters than enterprises.

A later study of around 400,000 sessions found a stable division of labor: people made most planning decisions about **what** to do, while the agent made most execution decisions about **how**. Greater domain expertise let users extract more work per instruction and recover from errors more effectively. The estimated value of a typical task rose about 25% over seven months.

These are vendor studies based on use of one product, not neutral measurements of the whole market. Their value is the observed interaction pattern, not a precise forecast.

**Engineering implication:** syntax proficiency remains necessary for reading and diagnosis, but problem formulation and domain judgment become stronger bottlenecks.

Sources:

- Anthropic Economic Index, [AI's impact on software development](https://www.anthropic.com/research/impact-software-development), 2025-04-28
- Anthropic, [Agentic coding and persistent returns to expertise](https://www.anthropic.com/research/claude-code-expertise), 2026-06-16

## Reliability and security: generation is ahead of assurance

SWE-bench Verified shows that agents can resolve a meaningful share of bounded real-world issues. It should not be read as proof that they can own a production service: repositories, tests and issue statements provide unusually clear boundaries.

Security is a separate capability. SECODEPLT covers more than 5,900 samples across 44 CWE-based risk categories and evaluates secure generation, vulnerability detection and patching with dynamic metrics. Its results show uneven strengths across those tasks. General coding ability does not imply reliable secure coding.

**Engineering implication:** scale generation only with stronger controls:

- tests derived from invariants;
- property-based and adversarial testing;
- static and dynamic analysis;
- least-privilege tools and isolated execution;
- reproducible traces and replay;
- explicit approval for costly or irreversible actions;
- canaries, rollback and incident-to-regression loops.

Sources:

- [SWE-bench Verified](https://www.swebench.com/verified)
- Nie et al., [SECODEPLT](https://proceedings.neurips.cc/paper_files/paper/2025/file/13d0a982aae786d473f6949b734e2720-Paper-Datasets_and_Benchmarks_Track.pdf), NeurIPS 2025

## A bounded projection

Assuming recent progress continues, the next 36 months likely bring:

- larger tasks that can be delegated when context and acceptance tests are clean;
- more concurrent agent work;
- lower cost for prototypes, migrations, tests and routine maintenance;
- heavier pressure on review, integration and operational ownership;
- greater advantage for teams with strong internal platforms, evals and feedback data;
- more products whose initial code is easy to copy.

It does **not** follow that:

- ambiguous product decisions become automatic;
- a 50% benchmark success rate is deployable reliability;
- more code means more customer value;
- a small engineering team implies a one-person company across sales, support and compliance;
- today's best tool or framework becomes a durable moat.

## Leading indicators to revisit quarterly

Track these rather than model marketing claims:

1. Longest task class completed at an acceptable success rate on your own work.
2. Acceptance without human rework.
3. Human active time per validated change.
4. Escaped defects and security findings per change.
5. Review queue age as generated output rises.
6. Ability to migrate model/provider without outcome regression.
7. Share of incidents that become executable regression tests.
