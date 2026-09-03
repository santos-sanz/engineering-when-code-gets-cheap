# Measurement system

## North star

> **Validated value delivered per hour of human attention**, subject to budgets for defects, cost and risk.

No single scalar captures engineering quality. Use a balanced scorecard and keep raw denominators visible.

## Scorecard

| Dimension | Metric | Why it matters |
|---|---|---|
| Outcome | Revenue, savings, cycle time or decision quality | Connects engineering to value |
| Human leverage | Active human minutes per accepted result | Measures real attention, not agent runtime |
| Quality | Accepted without rework; escaped defect rate | Detects review debt |
| Reliability | Completion, abstention, escalation, SLO attainment | Separates useful autonomy from reckless output |
| Risk | Critical incidents and expected loss | Weights failures by consequence |
| Cost | Cost per correct/useful result | Includes model, compute and human review |
| Adoption | Weekly active use, retention, workflow penetration | Proves behavior change |
| Learning | Incident-to-regression time; eval coverage | Measures whether the system improves |
| Portability | Regression delta after provider/model swap | Detects lock-in and brittle prompting |

## Definitions

### Accepted without rework

A result reaches its intended state without material human correction. Cosmetic edits should be reported separately. Define "material" before measuring.

### Human active time

Count time spent specifying, monitoring, reviewing, correcting and recovering. Do not count unattended runtime. Concurrent agents must not multiply the same human minute.

### Cost per useful result

Include model/tool calls, infrastructure, review, exception handling and support. Cheap tokens can still produce an expensive workflow.

### Escaped defect

A defect discovered after the agreed validation gate. Segment by severity. One security incident should not disappear inside a high volume of harmless tasks.

## Evaluation stack

Use four levels:

1. **Component:** schema validity, tool selection, retrieval or classification quality.
2. **Trajectory:** state transitions, retries, policy compliance and resource use.
3. **Task outcome:** whether the intended job was completed correctly.
4. **Business outcome:** whether the workflow changed cost, revenue, risk or user behavior.

A system can improve at level 1 and regress at level 4.

## Baseline protocol

Before changing the workflow:

- sample representative tasks and exceptions;
- measure current human time, quality and cost;
- define error severity and acceptable risk;
- freeze a holdout set;
- state kill criteria;
- log the model/tool configuration.

After deployment, compare cohorts or use staged rollout where possible. A before/after chart is weak evidence when task mix, demand or staffing changed.

## Weekly review

Record:

1. validated outcome delivered;
2. active human hours;
3. acceptance without rework;
4. escaped defects and incidents by severity;
5. cost per result;
6. active and retained users;
7. review queue age;
8. new regressions added from failures.

Then answer:

- Which task class became safely delegable?
- Where did human review catch nothing useful?
- Where did the agent create hidden work?
- Which failure should become an invariant or automated check?
- Which feature or abstraction should be removed?

## Quarterly capability test

Maintain a stable basket of real tasks across:

- greenfield implementation;
- existing-code change;
- debugging;
- migration;
- security-sensitive work;
- ambiguous product work.

For each agent/model version, compare success, human time, cost and defects. This personal benchmark matters more than a public leaderboard because it matches the actual environment and risk profile.

## Anti-metrics

Do not use these alone:

- lines of code;
- number of agents;
- token volume;
- commits or pull requests;
- benchmark pass rate without task distribution;
- demo completion;
- self-reported time saved;
- users invited rather than retained.
